# 4.2 Storage Services

Azure storage services provide capabilities for 

- Storing
- Accessing
- Managing data

on cloud.

## Azure Blob

- Unstructured data such as documents, photos, videos, web assets, and so on.

## Azure Disk

- Gives disk for Azure Virtual Machines, multiple performance tiers, based on requirements

## Azure Queue

- Designed for reliable messaging between components.

## Azure Files

- Manage file shares for cloud or on-premise requirement.

## Azure Table

- NoSQL database for storing semi structured data, like configs, user information.

> Everything except Azure disk has a endpoint, since disk is connected to the VM and rest of them is not. Meaning we can make API calls to these services and retrieve data from there.
> 

![image.png](image%201.png)

> HTTP is by default disabled on storage accounts.
>