---
title: "5.3 Authentication and Authorization"
layout: default
---

# 5.3 Authentication and Authorization

Authentication is a process of verifying you are who you claim to be. This involves various methods like usernames & passwords, Key cards, Biometrics, tokens, etc. It’s about verifying your identity.

Once we are recognized, i.e., authenticated…

Authorization comes into play.

This is where we get the level of privilege designated to our identity, this involves user roles, access controls, and specific rights.

![image.png](/assets/images/image-3.png)

### Azure’s Approach

- Azure employs Entra ID for robust authentication
- And uses role based access control in Azure to manage authorization with detailed policies and access rules.

### Benefits

- Enhanced security, only legitimate entities access the resources.
- Fine-Grained access control, this allows precise management for user actions and resource accessibility.
- Compliance and Governance, Azure ensures the network follows strict policies and regulations to keep your organization compliant with government bodies

### Use Cases

- User login authentication, ensuring only verified users and applications can gain access.
- Access control for Azure resources for authorization, keeping the environment secure and compliant.