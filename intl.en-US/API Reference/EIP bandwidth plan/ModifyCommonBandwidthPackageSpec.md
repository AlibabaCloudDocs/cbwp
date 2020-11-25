# ModifyCommonBandwidthPackageSpec

Modifies the maximum bandwidth of an EIP bandwidth plan.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=ModifyCommonBandwidthPackageSpec&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ModifyCommonBandwidthPackageSpec|The operation that you want to perform. Set the value to **ModifyCommonBandwidthPackageSpec**. |
|Bandwidth|String|Yes|100|The maximum bandwidth of the EIP bandwidth plan. Unit: Mbit/s. |
|BandwidthPackageId|String|Yes|cbwp-2ze2ic1xd2qeqk145\*\*\*\*|The ID of the EIP bandwidth plan. |
|RegionId|String|Yes|cn-hangzhou|The region to which the EIP bandwidth plan belongs.

 You can call the [DescribeRegions](~~36063~~) operation to query region IDs. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|7F129000-F929-4AF5-BE8D-BAE434C795306|The ID of the request. |

## Examples

Sample requests

```

https://vpc.aliyuncs.com/?Action=ModifyCommonBandwidthPackageSpec
&Bandwidth=100
&BandwidthPackageId=cbwp-2ze2ic1xd2qeqk145****
&RegionId=cn-hangzhou
&<Common request parameters>

```

Sample success responses

`XML` format

```
<ModifyCommonBandwidthPackageSpecResponse>
      <RequestId>7F129000-F929-4AF5-BE8D-BAE434C79530</RequestId>
</ModifyCommonBandwidthPackageSpecResponse>
```

`JSON` format

```
{
	"RequestId":"7F129000-F929-4AF5-BE8D-BAE434C795306"
}
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The error message returned because the specified region ID does not exist. Check whether the region ID is valid.|
|404|InvalidBandwidth.ValueNotSupported|The specified value of Bandwidth not supported.|The specified maximum bandwidth value is invalid.|
|404|BandwidthPackage.FinancialLocked|The specified BandwidthPackage has been Financail Lock.|The specified EIP bandwidth plan is locked due to an overdue payment.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

