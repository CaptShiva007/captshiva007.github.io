---
title: "8.1 Tools for Interacting with Azure"
layout: default
---

# 8.1 Tools for Interacting with Azure

There are various methods and tools to interact with Azure

- Azure Portal
- Azure PowerShell
- Azure Cloud Shell
- Azure CLI
- We also have SDKs and Native REST APIs.

## Azure Portal

It is a web based user friendly interface for managing all Azure services. It helps create, manage, and monitor all from a web application.

## Azure PowerShell

```powershell
New-AzStorageAccount `
		-ResourceGroupName MyResourceGroup `
		-Name mystorageaccount `
		-Location westus `
		-SkuName Standard_GRS
```

Azure PowerShell is a powerful module that provides commandlets to manage Azure resources directly from PowerShell command line.

It’s ideal for automating the complex repetitive tasks through scripting.

## Azure Cloud Shell

It’s a browser accessible shell, that delivers command-line experience for Azure management tasks. 

It’s preconfigured to directly access Azure resources and can be directly accessed from Azure portal.

## Azure CLI

```powershell
az storage account create \
		-n mystorageaccount \
		-g MyResourceGroup \
		-l westus \
		--sku standard_LRS
```

It’s a cross platform command line program that connects with Azure resources, mostly for Linux users.

### Choice

Choice can be based on the following

- Workflow
- Operating System
- Graphical vs Command-line interface

### Best Practices

- Azure Portal - Quick Tasks, Visual monitoring.
- Azure PowerShell - Automation
- Azure Cloud Shell - Preconfigured management environment