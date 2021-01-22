# Associate an ECS instance deployed in a classic network with an EIP bandwidth plan

This topic describes how to migrate an Elastic Compute Service \(ECS\) instance from a classic network to a Virtual Private Cloud \(VPC\) network, and then associate the ECS instance with an EIP bandwidth plan. This allows you to manage the public IP addresses in a uniform way.

Before you perform this task, make sure the following requirements are met:

-   An Alibaba Cloud account is created. If you do not have an Alibaba Cloud account, click [Create an Alibaba Cloud account](https://account.alibabacloud.com/register/intl_register.htm).
-   An EIP bandwidth plan is purchased. For more information, see [Create an EIP bandwidth plan](/intl.en-US/User Guide/Create an EIP bandwidth plan.md).

## Step 1: Migrate an ECS instance from a classic network to a network

VPC networks are isolated networks, which ensure higher network security. You can migrate ECS instances from a classic network to a VPC network. For more information, see [Migrate ECS instances](/intl.en-US/Best practices/Classic network-to-VPC migration/Migrate ECS instances.md).

## Step 2: Associate the migrated ECS instance with an EIP bandwidth plan

After the ECS instance is migrated from a classic network to a VPC network, you can use one of the following methods to associate the ECS instance with an EIP bandwidth plan. For more information about this step, see:

-   Associate the ECS instance with an EIP bandwidth plan when the ECS instance is not assigned a public IP address. For more information, see [Associate an ECS instance that is not assigned a public IP address with an EIP bandwidth plan](/intl.en-US/Best Practices/Associate an ECS instance that is not assigned a public IP address with an EIP bandwidth
         plan.md).
-   Associate the ECS instance with an EIP bandwidth plan when the ECS instance is assigned a public IP address. For more information, see [Associate an ECS instance that uses a public IP address with an EIP bandwidth plan](/intl.en-US/Best Practices/Associate an ECS instance that uses a public IP address with an EIP bandwidth plan.md).

