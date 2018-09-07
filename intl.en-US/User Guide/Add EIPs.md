# Add EIPs {#task_hjr_jlk_z2b .task}

After creating an Internet Shared Bandwidth instance, add Elastic IP Addresses \(EIPs\) to it to manage the Internet traffic.

Note the following before adding EIPs:

-   After an EIP is added to an Internet Shared Bandwidth instance, its original peak bandwidth is phased out and the bandwidth of the Internet Shared Bandwidth instance is used by the EIP.

-   After an EIP is added to an Internet Shared Bandwidth instance, its original billing method is stopped, the EIP becomes a public IP, and no traffic fee is charged.

    However, the instance fee of the EIP is still charged. Adding an EIP to an Internet Shared Bandwidth instance does not affect the charging of the EIP instance fee. If the EIP is bound to an ECS instance of the VPC network, no EIP instance is charged. Otherwise, you will be billed for the EIP instance fee.

-   You can add up to 20 EIPs to one Internet Shared Bandwidth instance. To add more EIPs, submit a ticket.


1.  Log on to the [Internet Shared Bandwidth console](https://vpcnext.console.aliyun.com/cbwp/cn-hongkong/cbwps). 
2.  Select the region of the target Internet Shared Bandwidth instance. 
3.  Find the target instance and click **Add IP**. 
    -   If there is no available EIP in the region, click **Buy EIP and Add to Bandwidth Package** and enter the number of EIPs to buy.

        The system automatically creates the specified amount of EIPs and add them to the Internet Shared Bandwidth instance.

    -   If you have available EIPs, click **Select from EIP list** and select the EIPs to add from the **Usable EIP list**.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/19039/153628680111049_en-US.png)


