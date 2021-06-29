# AddCommonBandwidthPackageIp

Adds an elastic IP address \(EIP\) to an EIP bandwidth plan.

## Description

When you call this operation, take note of the following limits:

-   Only a pay-as-you-go EIP can be added.
-   The EIP and the EIP bandwidth plan belong to the same region.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=AddCommonBandwidthPackageIp&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|AddCommonBandwidthPackageIp|The operation that you want to perform. Set the value to **AddCommonBandwidthPackageIp**. |
|BandwidthPackageId|String|Yes|cbwp-2ze2ic1xd2qeqasdf\*\*\*\*|The ID of the EIP bandwidth plan. |
|IpInstanceId|String|Yes|eip-2zeerraiwb7uqwed\*\*\*\*|The ID of the EIP.

 You can call the [DescribeEipAddresses](~~36018~~) operation to query region IDs. |
|RegionId|String|Yes|cn-hangzhou|The ID of the region where the EIP bandwidth plan is created.

 You can call the [DescribeRegions](~~36063~~) operation to query region IDs. |
|IpType|String|No|EIP|The type of the IP address. Set the value to **EIP**, which indicates that an EIP is added to the EIP bandwidth plan. |
|ClientToken|String|No|0c593ea1-3bea-11e9-b96b-88e9fe637760|The client token that is used to ensure the idempotence of the request. You can use the client to generate a token, but you must ensure that it is unique among different requests. The token can contain only ASCII characters and cannot exceed 64 characters in length. |

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
    "RequestId": "01FDDD49-C4B7-4D2A-A8E5-A93915C450A6"
}
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The error message returned because the specified region ID does not exist. Check whether the service is available in this region.|
|404|InvalidBandwidthPackageId.NotFound|The specified bandwidthPackageId does not exist in our records.|The error message returned because the specified ID of the EIP bandwidth plan does not exist. Check whether the specified ID is valid.|
|400|InvalidInstanceId.NotFound|The InstanceId is not found.|The error message returned because InstanceId is set to an invalid value.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

