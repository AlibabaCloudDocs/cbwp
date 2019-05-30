# Add EIPs {#task_hjr_jlk_z2b .task}

After creating an Internet Shared Bandwidth instance, add Elastic IP Addresses \(EIPs\) to it to manage the Internet traffic.

Note the following before adding EIPs:

-   After an EIP is added to an Internet Shared Bandwidth instance, its original peak bandwidth is phased out and the bandwidth of the Internet Shared Bandwidth instance is used by the EIP.

-   You can add up to 100 EIPs to one Internet Shared Bandwidth instance. To add more EIPs, open a ticket.

-   If the bill of an EIP is overdue, the EIP is automatically removed from the Internet Shared Bandwidth. You can renew the EIP and then add it manually.

-   If the bill of an Internet Shared Bandwidth is overdue, all EIPs are removed from the Internet Shared Bandwidth.


1.  Log on to the [Internet Shared Bandwidth console](https://vpcnext.console.aliyun.com/cbwp/cn-hongkong/cbwps).
2.  Select the region of the target Internet Shared Bandwidth instance.
3.  Find the target instance and click **Add IP**. 
    -   If there is no available EIP in the region, click **Buy EIP and Add to Bandwidth Package** and enter the number of EIPs to buy.

        The system automatically creates the specified amount of EIPs and add them to the Internet Shared Bandwidth instance.

    -   If you have available EIPs, click **Select from EIP list** and select the EIPs to add from the **Usable EIP list**.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/19039/155921563311049_en-US.png)


