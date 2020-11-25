# AddCommonBandwidthPackageIp

Adds an elastic IP address \(EIP\) to an EIP bandwidth plan.

## Description

Take note of the following limits before you call this operation:

-   Only pay-as-you-go EIPs can be added.
-   The EIPs and the EIP bandwidth plan must be deployed in the same region.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=AddCommonBandwidthPackageIp&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|AddCommonBandwidthPackageIp|The operation that you want to perform. Set the value to **AddCommonBandwidthPackageIp**. |
|BandwidthPackageId|String|Yes|cbwp-2ze2ic1xd2qeqasdf\*\*\*\*|The ID of the EIP bandwidth plan. |
|IpInstanceId|String|Yes|eip-2zeerraiwb7uqwed\*\*\*\*|The ID of the EIP.

 You can call the [DescribeEipAddresses](~~36018~~) operation to query the ID of the EIP. |
|RegionId|String|Yes|cn-hangzhou|The region where the EIP bandwidth plan is deployed.

 You can call the [DescribeRegions](~~36063~~) operation to query region IDs. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|01FDDD49-C4B7-4D2A-A8E5-A93915C450A6|The ID of the request. |

## Examples

Sample requests

```

http(s)://[Endpoint]/? Action=AddCommonBandwidthPackageIp
&BandwidthPackageId=cbwp-2ze2ic1xd2qeqasdf****
&IpInstanceId=eip-2zeerraiwb7uqwed****
&RegionId=cn-hangzhou
&<Common request parameters>

```

Sample success responses

`XML` format

```
<AddCommonBandwidthPackageIpResponse>
      <RequestId>01FDDD49-C4B7-4D2A-A8E5-A93915C450A6</RequestId>
</AddCommonBandwidthPackageIpResponse>
```

`JSON` format

```
{
	"RequestId":"01FDDD49-C4B7-4D2A-A8E5-A93915C450A6"
}
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The error message returned because the specified RegionId parameter does not exist. Check whether the region ID is valid.|
|404|InvalidBandwidthPackageId.NotFound|The specified bandwidthPackageId does not exist in our records.|The error message returned because the EIP bandwidth plan does not exist.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

