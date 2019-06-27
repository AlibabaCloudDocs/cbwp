# RemoveCommonBandwidthPackageIp {#reference_i4w_xmt_ndb .reference}

Removes an EIP from an Internet Shared Bandwidth instance.

## Debug {#apiExplorer .section}

By using [API Explorer](https://api.aliyun.com/#product=Vpc&api=DescribeVpcAttribute), you can easily debug APIs, automatically generate SDK code examples, and quickly search for APIs.

## Request parameters {#section_cch_pjg_mdb .section}

|Parameter|Type|Required?|Example value|Description |
|:--------|:---|:--------|-------------|:-----------|
|Action|String |Yes|RemoveCommonBandwidthPackageIp| The name of this action. Value: 

 RemoveCommonBandwidthPackageIp

 |
|BandwidthPackageId|String |Yes|cbwp-2ze2ic1xd2qeqk145pn4u| The ID of the Internet Shared Bandwidth instance.

 |
|IpInstanceId|String|No|eip-2zeerraiwb7uj6i0d0fo3| The ID of the EIP instance.

 To query the ID of the EIP instance, call DescribeEipAddresses.

 |
|RegionId|String |Yes|cn-hangzhou| The ID of the region where the Internet Shared Bandwidth instance is located.

 To query the region ID, call DescribeRegions.

 |

## Response parameters {#section_ugs_f1g_cz .section}

|Parameter|Type|Example value|Description|
|:--------|:---|-------------|:----------|
|RequestId|String|0876DAB2-6A86-479B-96BC-C5A2458568D2|The ID of the request.|

## Examples {#section_ix5_h1g_cz .section}

**Request example**

``` {#createVPCpub}

https://vpc.aliyuncs.com/?Action=RemoveCommonBandwidthPackageIp
&BandwidthPackageId=cbwp-2ze2ic1xd2qeqk145pn4u
&IpInstanceId=eip-2zeerraiwb7uj6i0d0fo3
&RegionId=cn-hangzhou
&<CommonParameters>

```

**Response example**

XML format

```
<RemoveCommonBandwidthPackageIpResponse>
  <RequestId>0876DAB2-6A86-479B-96BC-C5A2458568D2</RequestId>
</RemoveCommonBandwidthPackageIpResponse>

```

JSON format

```
{
	"RequestId":"0876DAB2-6A86-479B-96BC-C5A2458568D2"
}
```

## Error codes {#section_uk2_pdg_xgb .section}

|HTTP status code|Error code|Error message|Description|
|----------------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The specified region ID does not exist.|
|404|InvalidBandwidthPackageId.NotFound|The specified bandwidthPackageId does not exist in our records.|The specified Internet Shared Bandwidth instance does not exist.|

[See common error codes](https://error-center.aliyun.com/status/product/Vpc)

