# 6.1 Factors Affecting Cost

There are mainly six factors that affect the cost.

1. Type of resource
2. Consumption model
3. Lack of Maintenance
4. Region
5. Ingress and Egress
6. Type of Subscription

## Type of Resource

- Expenses are tailored to the specific service or asset that we’re using, in other words, Expenses = Consumption measured + Type of Asset.
    - There are different meters associated with each services, that’s what we use for calculating the cost of a resource.

## Consumption Model

- Azure operates in pay-as-you-go model. The level of usage stands as a primary factor in driving expenses.
    - For example, the virtual machine ran for 730 hours i.e. for a month, it’ll cost more, meanwhile shutting the VM when not in use, will significantly reduce the cost.
    - **Cost ∝ Usage**, the more we use , the more we pay.

## Lack of Maintenance

- Regular surveillance of Azure usage and proactive system management can lead to the discovery of expense and reduction in unnecessary expenses like decommissioning of seldom utilized virtual machines.
    - People usually start the services and forget about them. Sometimes the project is terminated but the resources will be under operation, leading to unnecessary expense.

## Region

- The cost of the resources can vary depending upon the location on which it is deployed.

## Ingress and Egress

- Ingress means incoming data transfer, while Egress means outgoing data transfer out of Azure network
    - Ingress is usually free
    - while Egress incurs a cost which can depend on the amount and destination.

## Types of Subscription

![image.png](image%2011.png)