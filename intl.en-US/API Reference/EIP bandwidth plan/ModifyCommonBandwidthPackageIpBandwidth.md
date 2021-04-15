# ModifyCommonBandwidthPackageIpBandwidth

Configures the bandwidth limit for an Elastic IP address that is added to an EIP bandwidth plan instance.

## API description

You can make this call to allocate the maximum available bandwidth of each Elastic IP address added to an EIP bandwidth plan instance. By doing so, you can avoid the bandwidth of the EIP bandwidth plan from being occupied by an Elastic IP address.

For example, if two Elastic IP addresses are added to an EIP bandwidth plan of 800 Mbit/s, you can set the bandwidth limit of the first Elastic IP address to 500 Mbit/s, and set the bandwidth limit of the other Elastic IP address to 400 Mbit/s. After the configuration is complete, the available bandwidth of the first Elastic IP address does not exceed 500 Mbit/s, and the available bandwidth of the second Elastic IP address does not exceed 400 Mbit/s.

Note the following before making this call: This action only takes effect when the Elastic IP address is associated with an Elastic Compute Service \(ECS\) instance, and does not take effect when the Elastic IP address is associated with a Server Load Balancer \(SLB\), NAT Gateway, secondary Elastic Network Interface \(ENI\), or a High-Availability Virtual IP Address \(HaVip\).

## Make the API call

[You can use OpenAPI Explorer to make API calls, search for API calls, perform debugging, and generate SDK example code.](https://api.aliyun.com/#product=Vpc&api=ModifyCommonBandwidthPackageIpBandwidth&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required?|Example value|Description|
|---------|----|---------|-------------|-----------|
|Action|String|Yes|ModifyCommonBandwidthPackageIpBandwidth|The name of this action. Value: **ModifyCommonBandwidthPackageIpBandwidth**. |
|Bandwidth|String|Yes|500|The maximum available bandwidth that can be allocated. Unit: Mbit/s. |
|BandwidthPackageId|String|Yes|cbwp-2zep6hw5d6y8exscd\*\*\*\*|The ID of the EIP bandwidth plan instance. |
|EipId|String|Yes|eip-2zewysoansu0svfbg\*\*\*\*|The ID of the Elastic IP address added to the EIP bandwidth plan instance. |
|RegionId|String|Yes|cn-hangzhou|The ID of the region to which the EIP bandwidth plan instance belongs. To query the region ID, call [DescribeRegions](~~36063~~). |

## Response parameters

|Parameter|Type|Example value|Description|
|---------|----|-------------|-----------|
|RequestId|String|63D187BF-A30A-4DD6-B68D-FF182C96D8A2|The ID of the request. |

## Examples

Request example

```
http(s)://vpc.aliyuncs.com/? Action=ModifyCommonBandwidthPackageIpBandwidth
&Bandwidth=500
&BandwidthPackageId=cbwp-2zep6hw5d6y8exscd****
&EipId=eip-2zewysoansu0svfbg****
&RegionId=cn-hangzhou
&<Common request parameters>
```

Response example

`XML` format

```
<ModifyCommonBandwidthPackageIpBandwidth>
      <RequestId>63D187BF-A30A-4DD6-B68D-FF182C96D8A2</RequestId>
</ModifyCommonBandwidthPackageIpBandwidth>
```

`JSON` format

```
{
    "RequestId": "63D187BF-A30A-4DD6-B68D-FF182C96D8A2"
}
```

## Errors

|HTTP status code|Error code|Error message|Description|
|----------------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The specified RegionId does not exist.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

