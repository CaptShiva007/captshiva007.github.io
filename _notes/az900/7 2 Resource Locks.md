---
title: "7.2 Resource Locks"
layout: default
---

# 7.2 Resource Locks

Resource lock acts as a safeguard helping you prevent accidental deletion or modification of Azure resources by placing a lock in various locks of the resource hierarchy, like subscriptions, resource groups, etc.

## Types

- Read-Only lock, allows users only read only access to resources.
- Delete lock, this ensures that a resource cannot be deleted, modifications are possible but deletion is not possible.

### Key Features

- Scope of Application, resource locks can be applied widely from entire subscriptions to individual resources.
- Flexible control, depending on need different lock can be used.

### Benefits

- Protection against accidental deletion.
- Customizable security
- Enhanced governance, supports governance principles.

### Use Cases

- Ideal for protecting critical resources
- Secure Prod databases
- Safeguard key network components.