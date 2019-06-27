# Add EIPs {#task_hjr_jlk_z2b .task}

After creating an Internet Shared Bandwidth instance, you need to add Elastic IP Addresses \(EIPs\) to it to manage Internet traffic.

Note the following before you add EIPs to an Internet Shared Bandwidth instance:

-   After an EIP is added to an Internet Shared Bandwidth instance, its original peak bandwidth becomes invalid. The bandwidth of the Internet Shared Bandwidth instance is used by the EIP.
-   After an EIP is added to an Internet shared bandwidth instance, the original billing method of the EIP becomes invalid. The EIP is changed to a public IP address. No additional EIP traffic fee is charged. However, the EIP instance fee is charged.
-   Adding an EIP to an Internet Shared Bandwidth instance does not affect the charging of the EIP instance fee. However, if the EIP is associated with an ECS instance of the VPC network, no EIP instance fee is charged. If the EIP is associated with a NAT Gateway, Server Load Balancer instance, secondary Elastic Network Interface, or High-Availability Virtual IP Address, the EIP instance fee is charged.
-   You can add up to 100 EIPs to each Internet Shared Bandwidth instance. To add more EIPs, open a ticket.
-   Overdue EIPs are automatically removed from an Internet Shared Bandwidth instance. All EIPs added to an Internet Shared Bandwidth instance are removed after the Internet Shared Bandwidth instance becomes overdue.

1.  Log on to the [VPC console](https://partners-intl.console.aliyun.com/#/vpc).
2.  In the left-side navigation pane, click **Internet Shared Bandwidth**.
3.  Select the region of the target Internet Shared Bandwidth instance.
4.  On the Internet Shared Bandwidth page, find the target instance, and click **Add IP** in the **Actions** column.
5.  On the Add IP page, add EIPs according to the following information and then click **OK**. 
    -   If no EIPs are available in the selected region, click the **Buy EIP and Add to Bandwidth Package** tab and enter the number of EIPs to buy.

        The system automatically creates the specified number of EIPs and add them to the Internet Shared Bandwidth instance.

    -   If EIPs are available in the selected region, click the **Select from EIP list** tab and select the EIPs to add from the **Usable EIP list**.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/19039/156163823611049_en-US.png)


