# DeleteCommonBandwidthPackage

You can call this operation to delete an EIP bandwidth plan.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=DeleteCommonBandwidthPackage&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteCommonBandwidthPackage|The operation that you want to perform. Set the value to **DeleteCommonBandwidthPackage**.

  |
|BandwidthPackageId|String|Yes|cbwp-2ze2ic1xd2qeqk145pn4u|The ID of the EIP bandwidth plan. |
|RegionId|String|Yes|cn-hangzhou|The region to which the EIP bandwidth plan belongs.

 You can call the [DescribeRegions](~~36063~~) operation to query region IDs. |
|Force|String|No|false|Indicates whether to forcibly delete the EIP bandwidth plan. Valid values:

 -   **False** \(default\): deletes the EIP bandwidth plan only if it is not associated with EIPs.
-   **True**: disassociates all EIPs from the EIP bandwidth plan and deletes the EIP bandwidth plan. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|B400EF57-60E3-4D61-B8FB-7FA8F72DF5A6|The ID of the request. |

## Examples

Sample requests

```

https://vpc.aliyuncs.com/?Action=DeleteCommonBandwidthPackage
&BandwidthPackageId=cbwp-2ze2ic1xd2qeqk145pn4u
&RegionId=cn-hangzhou
&<Common request parameters>

```

Sample success responses

`XML` format

```
<DeleteCommonBandwidthPackageResponse>
      <RequestId>B400EF57-60E3-4D61-B8FB-7FA8F72DF5A6</RequestId>
</DeleteCommonBandwidthPackageResponse>
```

`JSON` format

```
{
	"RequestId":"B400EF57-60E3-4D61-B8FB-7FA8F72DF5A6"
}
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The error message returned because the specified region ID does not exist.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

