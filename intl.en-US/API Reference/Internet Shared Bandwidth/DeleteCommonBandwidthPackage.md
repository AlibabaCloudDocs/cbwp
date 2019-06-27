# DeleteCommonBandwidthPackage {#reference_i4w_xmt_ndb .reference}

Deletes an Internet Shared Bandwidth instance.

## Debug {#apiExplorer .section}

By using [API Explorer](https://api.aliyun.com/#product=Vpc&api=DescribeVpcAttribute), you can easily debug APIs, automatically generate SDK code examples, and quickly search for APIs.

## Request parameters {#section_cch_pjg_mdb .section}

|Parameter|Type|Required?|Example value|Description |
|:--------|:---|:--------|-------------|:-----------|
|Action|String|Yes|DeleteCommonBandwidthPackage| The name of this action. Value: 

 DeleteCommonBandwidthPackage

 |
|BandwidthPackageId|String |Yes|cbwp-2ze2ic1xd2qeqk145pn4u| The ID of the Internet Shared Bandwidth instance.

 |
|RegionId|String |Yes|cn-hangzhou| The ID of the region where the Internet Shared Bandwidth instance is located.

 To query the region ID, call DescribeRegions.

 |
|Force|Boolean|No|false| Indicates whether to forcibly delete the Internet Shared Bandwidth instance. Valid values:

 -   false: Does not forcibly delete the Internet Shared Bandwidth instance if it contains EIP.
-   true: Forcibly remove all EIPs in the Internet Shared Bandwidth instance and then delete the Internet Shared Bandwidth instance.

 |

## Response parameters {#section_ugs_f1g_cz .section}

|Parameter|Type|Example value|Description|
|:--------|:---|-------------|:----------|
|RequestId|String|B400EF57-60E3-4D61-B8FB-7FA8F72DF5A6|The ID of the request.|

## Examples {#section_ix5_h1g_cz .section}

**Request example**

``` {#createVPCpub}

https://vpc.aliyuncs.com/?Action=DeleteCommonBandwidthPackage
&BandwidthPackageId=cbwp-2ze2ic1xd2qeqk145pn4u
&RegionId=cn-hangzhou
&<CommonParameters>

```

**Response example**

XML format

```
<DeleteCommonBandwidthPackageResponse>
  <RequestId>B400EF57-60E3-4D61-B8FB-7FA8F72DF5A6</RequestId>
</DeleteCommonBandwidthPackageResponse>

```

JSON format

```
{
	"RequestId":"B400EF57-60E3-4D61-B8FB-7FA8F72DF5A6"
}
```

## Error codes {#section_kp4_gwf_xgb .section}

|HTTP status code|Error code|Error message|Description|
|----------------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The specified region ID does not exist.|

[See common error codes](https://error-center.aliyun.com/status/product/Vpc)

