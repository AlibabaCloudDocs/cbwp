# Use Internet Shared Bandwidth to simplify the management of the Internet egress {#concept_rh1_qgy_b2b .concept}

You can add EIPs in a region to an Internet Shared Bandwidth instance to uniformly manage the Internet egress. You can adjust the peak bandwidth at any time to handle traffic fluctuation.

## Add an ECS instance without an EIP to Internet Shared Bandwidth {#section_d1f_vgy_b2b .section}

If you do not have an available EIP, you can create an EIP when adding it to an Internet Shared Bandwidth instance, and then bind the EIP to a cloud resource.

To create an EIP and add it to Internet Shared Bandwidth, complete these steps:

1.  Log on to the [Internet Shared Bandwidth console](https://vpcnext.console.aliyun.com/cbwp/cn-hongkong/cbwps).
2.  Select the region of the ECS instance, and click **Buy Internet Shared Bandwidth**.
3.  Select the billing method and peak bandwidth on the purchase page according to your needs and complete the payment.

    For more information, see .

4.  Find the newly created Internet Shared Bandwidth and click **Add IP**.
5.  On the Add IP page, click **Buy EIP and add to Bandwidth Package**.

    The system automatically creates the specified amount of EIPs and adds them to the Internet Shared Bandwidth instance.

    ![](images/6207_en-US.png)

6.  Find the newly created Internet Shared Bandwidth, and click **Manage** in the **Actions** column.

    ![](images/6208_en-US.png)

7.  In the left-side navigation pane, click **Shared Bandwidth IPs**, find the newly added EIP and click **Bind**.

    ![](images/6209_en-US.png)

8.  In the displayed dialog box, complete these steps:
    1.  In the **Instance Type** list, select **ECS Instance**.
    2.  Select the ECS instance to bind and click **OK**.

## Add an ECS instance bound with an EIP to Internet Shared Bandwidth {#section_gph_bjy_b2b .section}

If your ECS instance is already bound with an EIP, you only need to add the EIP of the ECS instance to an Internet Shared Bandwidth instance to manage the Internet bandwidth of the ECS instance.

1.  Log on to the [Internet Shared Bandwidth console](https://vpcnext.console.aliyun.com/cbwp/cn-hongkong/cbwps).
2.  Select the region of the Internet Shared Bandwidth.
3.  Find the target Internet Shared Bandwidth instance and click **Add IP**.
4.  On the Add IP page, click **Select from EIP list**.

    **Note:** After the EIP is added to the Internet Shared Bandwidth instance, its peak bandwidth becomes that of the instance. Meanwhile, billing on the EIP stops and no traffic fee is charged on the EIP.


## Add an ECS instance with a public IP to Internet Shared Bandwidth {#section_rks_sjy_b2b .section}

If your ECS instance uses an allocated public IP, you can change it to an EIP and then add the EIP to Internet Shared Bandwidth.

1.  Log on to the [ECS console](https://ecs.console.aliyun.com/#/server/).
2.  Select the region of your ECS instance.
3.  Find your ECS instance, click **More** \> **Network and Security Group** \> **Convert to EIP**. In the displayed dialog box, click **OK**.

    ![](images/6212_en-US.png)

4.  Refer to [Add an ECS instance bound with an EIP to Internet Shared Bandwidth](#section_gph_bjy_b2b) to add the ECS instance to Internet Shared Bandwidth.

