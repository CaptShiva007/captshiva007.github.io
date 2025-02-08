---
title: "3.1.4 Azure Container Services"
layout: default
---

# 3.1.4 Azure Container Services

### Difference between VMs and Containers

| **VMs** | **Container** |
| --- | --- |
| Runs on Hypervisor | Runs on Container Runtime |
| Resource intensive | Resource extensive |
| Sets up a guest OS for operation | Does not need a guest OS  |
| Not as much as Container | Isolated and runs in user mode |
| Kinda hard to deploy than Container | Easier deployment |
|  | Persistent storage |
|  | Has fault tolerance |

![image.png](/assets/images/image-18.png)

---

### Azure Container Services

- Offers streamlined and lightweight virtual environment for service deployment.
- No OS management required.
- They’re designed to be responsive and adaptive. Can change with respect to demand.

### Types:

1. Azure Container Instance
2. Azure Container Apps
3. Azure Kubernetes Service

# 1. Azure Container Instances:

- Azure container instance is a PaaS offering that simplifies the process of running container in cloud.
- Designed for developers who doesn’t want to worry about the overhead of orchestrating container deployments.
- No VM management needed. Since its PaaS, its managed by the Microsoft.
- It offers fast and simple deployment. VMs takes 2-3 minutes, containers get the job done in 30 secs.

### Key Features:

- Ease of deployment. No complex orchestration.
- No need to configure VMs, independent instances.
- Flexible sizing, we can allocate memory and CPU depending on the need by the container.

### Benefits:

- Simplicity and speed, streamlined for quick deployments.
- Cost efficient, pay as you go model.
- Secure and isolated, ensuring security from external threats, and other running containers.

### Use Cases

- Ideal for simple applications.
- Fast and efficient execution and isolated.
- Suitable for task automation and build jobs and scenarios for quick iterations and deployments are needed.

# Azure Container Apps:

- It’s a PaaS offering.
- That is designed to scale and deploy modern applications.
- Microservices using containers.

> Azure container apps, built on simplicity of Azure container instance with additional features from other complex applications.
> 

### Difference between Azure container instances and Azure container apps:

Container instances are for single containers, while Container apps take it a step further to provide a platform for running multiple containers with orchestration features for microservice architecture. 

> Microservice architecture: Every service in an application will be run inside a container, so instead of having a bigger single application model, aka monolith, we are breaking it down into smaller services called the microservices.
> 

### Key Features:

- Scalability, Applications can adapt to user traffic in real-time.
- They’re an ideal choice for microservice architecture, which offers built-in service discovery and traffic routing.
- Container apps ensure continuous integration and delivery pipelines, which helps streamline the development process.

### Benefits:

- Simplified Management, we can just focus on the code not on the systems(courtesy of PaaS).
- Scalability and flexibility, you can respond to changes in traffic and resource demands dynamically.
- Cost effectiveness, pay only for what we use.

### Use Cases:

Ideal for modern apps that demand scalability and flexibility such as web apps, and event-driven architectures.

# Azure Kubernetes Service:

AKS is designed for applications that requires complex orchestrations, auto-scaling and multi container management, which surpasses the capabilities of Azure container instances and apps, when it comes to managing microservices and large scale applications.

## What is Kubernetes?

Kubernetes is a open source orchestration platform or system for automating deployment, scaling, management of containerized application.

### Key Features:

- Automated Kubernetes management, AKS saves time and efforts.
- Integrated developer tools, such as Azure DevOps, and other popular tools, making it developer perfect.
- Advanced networking feature that ensures applications perform optimally at any scale.

### Benefits:

- Simplified deployment, streamlines Kubernetes management.
- Scalability, up or down on demand.
- Security and Compliance.

### Use Case:

- AKS is perfect for businesses that require high availability.
- That requires scalable microservices.
- It also supports versatile architectures.