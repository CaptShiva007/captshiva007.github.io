---
title: "8.4 Infrastructure as a Code"
layout: default
---

# 8.4 Infrastructure as a Code

IaaC is a key DevOps practice that involves managing, provisioning the resources with the help of machine readable definition files rather than manually doing it or using interactive configuration tools.

### Components of IaaC

- Azure Resource Manager Templates, JSON files that define the resources that you want to deploy.
- Azure Bicep, Its a domain specific language that deploys Azure resources declaratively and its easier to understand than ARM templates.
- Terraform, tool used within Azure to define, preview, and deploy cloud infrastructure with declarative configuration file.

> Terraform is a courtesy of HashiCorp and written in HashiCorp Configuration Language (HCL). We can use Terraform to deploy in AWS, GCP and other cloud providers. But ARM templates and Bicep is specific for Azure.
> 

### Benefits

- Speed and Simplicity, IaaC enables you to quickly rollout and manage infrastructure with minimal manual intervention.
- Consistency and Accuracy, IaaC prevents environmental drift and reduce manual errors
- Reusability and scalability

### Use Cases

- Automated environment setup
- Managing multi-cloud environment
- Implementing DevOps practices

# ARM Templates

ARM Templates are JSON files that define the resources you need for your cloud application in Azure. They allow to deploy a wide array of resources together in a coordinated manner.

### Key Features

- Declarative Syntax
- Idempotency, we can deploy the templates numerous times being confident that they’ll produce the same environment each time. Meaning its reliable and stable.
- Modularity, templates can be modular.

### Benefits

- Automation and Scalability
- Consistency
- Source Control

### Use Cases

- Development
- Testing
- Staging
- Production

![image.png](image%2014.png)

 

# Bicep

Domain specific language for deploying Azure resources declaratively. Simplifies the authoring experience.

### Key Features

- Simplified syntax, easy to read and write.
- First-class tooling, integrated support in VSCode and in Azure CLI
- No state or state files, Bicep offers direct integration with Azure resource manager.

![image.png](image%2015.png)

### Benefits

- Easier to understand
- Less boilerplate code
- Transparent abstraction, the bicep script actually converts into ARM template, but its not visible and its not relevant for us. It just makes it easier for us to write ARM template.
- Strong typing and validation

### Use Cases

- Efficiently resource provisioning
- Reliable Azure resource deployment
- Targeted at developers and cloud engineers

![image.png](/assets/images/image-16.png)