# ModifyCommonBandwidthPackageAttribute

You can call this operation to modify the name and description of an EIP bandwidth plan.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer automatically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=ModifyCommonBandwidthPackageAttribute&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ModifyCommonBandwidthPackageAttribute|The operation that you want to perform. Set the value to: Yes

**ModifyCommonBandwidthPackageAttribute** |
|BandwidthPackageId|String| |cbwp-2ze2ic1xd2qeqk145pn4u|The ID of the EIP bandwidth plan. |
|RegionId|String|Yes|cn-hangzhou|The ID of the region to which the EIP bandwidth plan belongs.

You can call the [DescribeRegions](~~36063~~) operation to query region IDs. |
|Description|String|No|Description|The description of the EIP bandwidth plan. The description must be 2 to 256 characters in length. It must start with a letter but cannot start with `http://` or `https://`. |
|Name|String|No|test123|The name of the EIP bandwidth plan. The name must be 2 to 128 characters in length and can contain letters, digits, periods \(.\), underscores \(\_\), and hyphens \(-\). It must start with a letter but cannot start with`http://` or `https://`. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|B450CAD8-50BC-4506-ADA7-35C6CE63E96B|The ID of the request. |

## Examples

Sample requests

```

https://vpc.aliyuncs.com/?BandwidthPackageId=cbwp-2ze2ic1xd2qeqk145pn4u
&RegionId=cn-hangzhou
&<Common request parameters>

```

Sample success responses

`XML` format

```
<ModifyCommonBandwidthPackageAttributeResponse>
      <RequestId>B450CAD8-50BC-4506-ADA7-35C6CE63E96B</RequestId>
</ModifyCommonBandwidthPackageAttributeResponse>
```

`JSON` format

```
{
	"RequestId":"B450CAD8-50BC-4506-ADA7-35C6CE63E96B6"
}
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The error message returned because the specified region ID does not exist.|
|404|InvalidBandwidthPackageId.NotFound|The specified bandwidthPackageId does not exist in our records.|The error message returned because the specified EIP bandwidth plan does not exist.|
|400|InvalidParameter.Name.Malformed|The specified Name is not valid.|The error message returned because the specified name is invalid.|
|400|InvalidParameter.Description.Malformed|The specified Description is not valid.|The error message returned because the specified description is invalid.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

