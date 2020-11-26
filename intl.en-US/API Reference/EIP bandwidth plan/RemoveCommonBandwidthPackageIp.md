# RemoveCommonBandwidthPackageIp

You can call this operation to disassociate an elastic IP address \(EIP\) from an EIP bandwidth plan.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=RemoveCommonBandwidthPackageIp&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|RemoveCommonBandwidthPackageIp|The operation that you want to perform. Set the value to **RemoveCommonBandwidthPackageIp**.

  |
|BandwidthPackageId|String|Yes|cbwp-2ze2ic1xd2qeqk145pn4u|The ID of the EIP bandwidth plan. |
|IpInstanceId|String|Yes|eip-2zeerraiwb7uj6i0d0fo3|The ID of the EIP.

 You can call the [DescribeEipAddresses](~~36018~~) operation to query the ID of the EIP. |
|RegionId|String|Yes|cn-hangzhou|The region to which the EIP bandwidth plan belongs.

 You can call the [DescribeRegions](~~36063~~) operation to query region IDs. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|0876DAB2-6A86-479B-96BC-C5A2458568D2|The ID of the request. |

## Examples

Sample requests

```

https://vpc.aliyuncs.com/?Action=RemoveCommonBandwidthPackageIp
&BandwidthPackageId=cbwp-2ze2ic1xd2qeqk145pn4u
&IpInstanceId=eip-2zeerraiwb7uj6i0d0fo3
&RegionId=cn-hangzhou
&<Common request parameters>

```

Sample success responses

`XML` format

```
<RemoveCommonBandwidthPackageIpResponse>
      <RequestId>0876DAB2-6A86-479B-96BC-C5A2458568D2</RequestId>
</RemoveCommonBandwidthPackageIpResponse>
```

`JSON` format

```
{
	"RequestId":"0876DAB2-6A86-479B-96BC-C5A2458568D2"
}
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The error message returned because the specified region ID does not exist.|
|404|InvalidBandwidthPackageId.NotFound|The specified bandwidthPackageId does not exist in our records.|The error message returned because the EIP bandwidth plan does not exist.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

