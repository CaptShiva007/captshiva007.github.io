---
title: "8.3 Azure Resource Manager"
layout: default
---

# 8.3 Azure Resource Manager

The request we are submitting from Azure Portal, CLI, PowerShell, or from REST client, it goes to Azure Resource Manger (ARM), it is a deployment and management service for Azure. It provides a management layer that allows us to update, delete resources in the Azure network.

![image.png](/assets/images/image-13.png)

For every resource there is a resource provider

for example 

if you take VM, its `Microsoft.Compute` 

for web apps, `Microsoft.Web`

for databases, `Microsoft.SQLDatabase`

All of this is handled in the background by ARM.

> ARM was previously called as Azure Service manager, resources created through ASM called classic resources.
