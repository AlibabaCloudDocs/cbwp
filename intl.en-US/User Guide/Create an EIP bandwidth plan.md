# Create an EIP bandwidth plan

After you create an EIP bandwidth plan, you can associate it with one or more EIPs in the same region. This allows you to manage public IP addresses in a uniform way and ensure a maximum bandwidth at the Gbit/s level.

1.  Log on to the [EIP bandwidth plan console](https://vpc.console.aliyun.com/cbwp/cn-hangzhou/cbwps).

2.  On the **Internet Shared Bandwidth** page, click **Buy Internet Shared Bandwidth**.

3.  On the buy page, set the following parameters for an EIP bandwidth plan, click **Buy Now**, and then complete the payment.

    |Parameter|Description|
    |---------|-----------|
    |**Region**|Select the region where you want to create the EIP bandwidth plan. Make sure that the EIP bandwidth plan is created in the same region as the EIP you want to associate with. |
    |**Line type**|Select the line type of the EIP bandwidth plan.     -   **BGP \(Multi-ISP\)**: If you select this option, you can associate only EIPs of BGP \(Multi-ISP\) with the EIP bandwidth plan.
    -   **BGP \(Multi-ISP\)\_PRO**: If you select this option, you can associate only EIPs of BGP \(Multi-ISP\)\_PRO with the EIP bandwidth plan.

**Note:** Only China \(Hong Kong\) supports BGP \(Multi-ISP\)\_PRO. |
    |**Billing method**|Select the billing method of the EIP bandwidth plan. Only pay-as-you-go is supported. For more information, see [Billing](/intl.en-US/Pricing/Billing.md). |
    |**Bandwidth**|Select the bandwidth of the EIP bandwidth plan.|
    |**Name**|Enter the name of the EIP bandwidth plan. The name must be 2 to 128 characters in length and can contain letters, Chinese characters, digits, underscores \(\_\), and hyphens \(-\). It must start with a letter or a Chinese character. |
    |**Quantity**|Specify the number of EIP bandwidth plans that you want to purchase.|


[Add EIPs](/intl.en-US/User Guide/Add EIPs.md)

**Related topics**  


[CreateCommonBandwidthPackage](/intl.en-US/API reference/EIP bandwidth plan/CreateCommonBandwidthPackage.md)

