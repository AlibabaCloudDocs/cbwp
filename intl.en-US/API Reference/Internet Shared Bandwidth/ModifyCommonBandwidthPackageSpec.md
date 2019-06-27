# ModifyCommonBandwidthPackageSpec {#reference_i4w_xmt_ndb .reference}

Modifies the peak bandwidth of an Internet Shared Bandwidth instance.

## Debug {#apiExplorer .section}

By using [API Explorer](https://api.aliyun.com/#product=Vpc&api=DescribeVpcAttribute), you can easily debug APIs, automatically generate SDK code examples, and quickly search for APIs.

## Request parameters {#section_cch_pjg_mdb .section}

|Parameter|Type|Required?|Example value|Description |
|:--------|:---|:--------|-------------|:-----------|
|Action|String |Yes|ModifyCommonBandwidthPackageSpec| The name of the action. Value: 

 ModifyCommonBandwidthPackageSpec

 |
|Bandwidth|Integer|Yes|100| The peak bandwidth in Mbps of the Internet Shared Bandwidth instance.

 |
|BandwidthPackageId|String |Yes|cbwp-2ze2ic1xd2qeqk145pn4u| The ID of the Internet Shared Bandwidth instance.

 |
|RegionId|String |Yes|cn-hangzhou|The ID of the region where the Internet Shared Bandwidth instance is located.To query the region ID, call DescribeRegions.

|

## Response parameters {#section_ugs_f1g_cz .section}

|Parameter|Type|Example value|Description|
|:--------|:---|-------------|:----------|
|RequestId|String|7F129000-F929-4AF5-BE8D-BAE434C795306|The ID of the request.|

## Examples {#section_ix5_h1g_cz .section}

**Request example**

``` {#ModifyVpnGatewayAttribute1}

https://vpc.aliyuncs.com/?Action=ModifyCommonBandwidthPackageSpec
&Bandwidth=100
&BandwidthPackageId=cbwp-2ze2ic1xd2qeqk145pn4u
&RegionId=cn-hangzhou
&<CommonParameters>

```

**Response example**

XML format

```
<ModifyCommonBandwidthPackageSpecResponse>
  <RequestId>7F129000-F929-4AF5-BE8D-BAE434C79530</RequestId>
</ModifyCommonBandwidthPackageSpecResponse>

```

JSON format

```
{
	"RequestId":"7F129000-F929-4AF5-BE8D-BAE434C795306"
}
```

## Error codes {#section_ijm_yyf_xgb .section}

|HTTP status code|Error code|Error message|Description|
|----------------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The specified region ID does not exist.|
|404|InvalidBandwidth.ValueNotSupported|The specified value of Bandwidth not supported.|The specified peak bandwidth value is not supported.|
|404|BandwidthPackage.FinancialLocked|The specified BandwidthPackage has been Financail Lock.|The specified Internet Shared Bandwidth is locked due to an insufficient balance.|

[See common error codes](https://error-center.aliyun.com/status/product/Vpc)

