---
title: "5.2 Microsoft Entra Domain Services"
layout: default
---

# 5.2 Microsoft Entra Domain Services

It is a directory service, a phone book for a computer network. A directory lists computers and users and resources on a network and their details. It’s necessary for managing and controlling access to resources in a network. 

Entra Domain service is a modern managed domain service. No need to worry about the infrastructure, and just deploy. It’s on cloud active directory.

- Managed domain service.
- Scalable and high availability.
- Compatibility with the Windows Server.

### Key Features

- Domain join, this allows Windows servers and computers to join a secure domain without the need for traditional domain controller. This makes it easier to manage network’s identity infrastructure.
- Group policy, with group policy you can manage your network users and computers efficiently. We can apply the security settings and configurations across the board.
- LDAP and Kerberos/NTLM Authentication, These are critical for supporting legacy protocols that are necessary for a wide range of applications and services to function securely and reliably. Traditional AD uses LDAP for directory services and Kerberos for authentication.

> Entra ID uses modern authentication protocols such as OpenID, OAuth, and SAML and so on.
> 
- Integrated management, can integrate the existing services with Entra ID.

### Benefits

- Simplified Administration, less time and resources spent on domain controllers.
- Scalability and Reliability, ensures domain service grows with organization’s growth.
- Security and Compliance, secure management of domain services following the industry compliant standards.

### Use Cases

- Active Directory Migration, to migrate from on-premises to Azure Cloud.
- Maintain the group policy without starting over again
- Also supports legacy applications.