---
title: "5.5 Conditional Access"
layout: default
---

# 5.5 Conditional Access

Conditional access is a security feature in Azure that helps enforce access controls on cloud applications based on specific conditions or criteria.

The process begins with the signals, these are pieces of information, to make a decision like a security check, the signals include user and their location, device they’re using using is secure and compliant, browser they’re using, and real-time risk. 

> Whenever we sign in Azure collects the sign in information and it builds something called a usage pattern. Whenever there’s a deviation from the usage pattern, that will be considered as a real-time risk.
> 

Once Azure has these signals, it proceeds to verify each of these attempt phase, this is the decision making step where Azure can allow access, or require MFA, or block access attempt.

This ensures that only the right people under the right conditional circumstances can access the valuable resources in Azure.

 

![image.png](/assets/images/image-4.png)

### Key Features

- Users and group based policies, these policies allow us to tailor access for specific users or groups.
- Location based policies, Access can be requested or allowed based on user location.
- Device based policies, policies can depend on whether or not the device is compliant or not.
- Risk based policies, its integrated with Azure Risk Detection. Security system that adapts based on the threat level.

### Benefits

- Enhanced security, ensures only the right person under the right conditions can access the network.
- Flexibility and control, we can tailor policies depending on the need.
- Streamlined user experience, reduces unnecessary hurdles for legit users while keeping out unauthorized users.

### Use Cases

- Protecting sensitive data
- Remote work and BYOD policy.