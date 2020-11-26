# CancelCommonBandwidthPackageIpBandwidth

You can call this operation to remove the bandwidth limit for an elastic IP address \(EIP\) that is associated with an EIP bandwidth plan.

After you remove the bandwidth limit, the maximum bandwidth of the EIP equals that of the EIP bandwidth plan.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=CancelCommonBandwidthPackageIpBandwidth&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CancelCommonBandwidthPackageIpBandwidth|The operation that you want to perform. Set the value to **CancelCommonBandwidthPackageIpBandwidth**. |
|BandwidthPackageId|String|Yes|cbwp-bp13d0m4e2qv8xxxxxxxx|The ID of the EIP bandwidth plan. |
|EipId|String|Yes|eip-2zewysoansu0sxxxxxxxx|The ID of the EIP that is associated with the EIP bandwidth plan. |
|RegionId|String|Yes|cn-hangzhou|The ID of the region to which the EIP bandwidth plan belongs. To query region IDs, call the [DescribeRegions](~~36063~~) operation. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|63D187BF-A30A-4DD6-B68D-FF182C96D8A2|The ID of the request. |

## Examples

Sample requests

```

https://vpc.aliyuncs.com/?Action=CancelCommonBandwidthPackageIpBandwidth
&BandwidthPackageId=cbwp-bp13d0m4e2qv8xxxxxxxx
&EipId=eip-2zewysoansu0sxxxxxxxx
&RegionId=cn-hangzhou
&<Common request parameters>

```

Sample success responses

`XML` format

```
<CancelCommonBandwidthPackageIpBandwidth>
	  <RequestId>63D187BF-A30A-4DD6-B68D-FF182C96D8A2</RequestId>
</CancelCommonBandwidthPackageIpBandwidth>
```

`JSON` format

```
{
	"RequestId":"63D187BF-A30A-4DD6-B68D-FF182C96D8A2"
}
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The error message returned because the specified region ID does not exist.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

