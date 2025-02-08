---
title: "5.7 Role Based Access Control (RBAC)"
layout: default
---

# 5.7 Role Based Access Control (RBAC)

The Entra ID comprises of various objects or entities such as users, groups, services, etc.

> Service principals are necessary to automate tasks to avoid user intervention.
> 

![image.png](/assets/images/image-7.png)

RBAC is used by users, service principals, and groups to authorize access to the Azure subscription and resources.

For role assignment we have to answer for three questions, such as,

- Who - who is the entity, user, group or service principal.
- Where - where do they want access
- What - What action would they like to perform

![image.png](/assets/images/image-8.png)

### Key Features

- Predefined roles - such as owner, contributor, reader, etc
- Custom roles - we can create custom role with custom permissions and responsibilities.
- Scope of Access - Where the roles can be assigned, and their limitations, inheritance to the lower levels.

### Benefits

- Least privilege - It follows the Principle Of Least Privilege, this minimizes the risk.
- Streamlined Management - Simplified user and permission management.
- Improved Compliance - Helps maintain necessary compliance standards.

### Use Cases

- Multi user environments
- Larger organizations
- Projects requiring strict access control

---

To boil it down,

1. Azure RBAC ensures strong safeguards by defining who can do what within the Azure environment.
2. Authentication with Entra ID gets you inside, but without RBAC authorization, you can do nothing.
3. Entra ID helps access, RBAC enables daily tasks.