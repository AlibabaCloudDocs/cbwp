# Create an EIP bandwidth plan

After you create an EIP bandwidth plan, you can associate it with one or more elastic IP addresses \(EIPs\). This allows you to manage EIPs in a centralized way and ensures a maximum bandwidth value at the Gbit/s level.

1.  Log on to the [EIP bandwidth plan console](https://vpc.console.aliyun.com/cbwp/cn-hangzhou/cbwps).

2.  On the **Internet Shared Bandwidth** page, click **Buy Internet Shared Bandwidth**.

3.  On the buy page, set the following parameters, click **Buy Now**, and then complete the payment.

    |Parameter|Description|
    |---------|-----------|
    |**Region**|Select the region where you want to create the EIP bandwidth plan. Make sure that the EIP bandwidth plan is created in the same region as the EIP you want to associate with. |
    |**Line Type**|Select the line type of the EIP bandwidth plan.     -   **BGP \(Multi-ISP\)**: If you select this option, you can associate only EIPs of BGP \(Multi-ISP\) with the EIP bandwidth plan.
    -   **BGP \(Multi-ISP\)\_PRO**: If you select this option, you can associate only EIPs of BGP \(Multi-ISP\)\_PRO with the EIP bandwidth plan.

**Note:** Only the China \(Hong Kong\) region supports BGP \(Multi-ISP\)\_PRO. |
    |**Billing method**|Select the billing method of the EIP bandwidth plan. Only pay-by-data-transfer is supported. For more information, see [Billing](/intl.en-US/Pricing/Billing.md). |
    |**Bandwidth**|Select the bandwidth value of the EIP bandwidth plan.|
    |**Name**|Enter a name for the EIP bandwidth plan. The name must be 2 to 128 characters in length and can contain digits, underscores \(\_\), and hyphens \(-\). It must start with a letter. |
    |**Purchase Quantity**|Specify the number of EIP bandwidth plans that you want to purchase.|


[Add EIPs](/intl.en-US/User Guide/Add EIPs.md)

**Related topics**  


[CreateCommonBandwidthPackage](/intl.en-US/API reference/EIP bandwidth plan/CreateCommonBandwidthPackage.md)

