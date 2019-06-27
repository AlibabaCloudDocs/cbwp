# ModifyCommonBandwidthPackageAttribute {#reference_i4w_xmt_ndb .reference}

Modifies the name and description of an Internet Shared Bandwidth instance.

## Debug {#apiExplorer .section}

By using [API Explorer](https://api.aliyun.com/#product=Vpc&api=DescribeVpcAttribute), you can easily debug APIs, automatically generate SDK code examples, and quickly search for APIs.

## Request parameters {#section_cch_pjg_mdb .section}

|Parameter|Type|Required?|Example value|Description |
|:--------|:---|:--------|-------------|:-----------|
|Action|String |Yes|ModifyCommonBandwidthPackageAttribute| The name of this action. Value:

 ModifyCommonBandwidthPackageAttribute

 |
|BandwidthPackageId|String |Yes|cbwp-2ze2ic1xd2qeqk145pn4u| The ID of the Internet Shared Bandwidth instance.

 |
|RegionId|String|Yes|cn-hangzhou|The ID of the region where the Internet Shared Bandwidth instance is located.To query the region ID, call DescribeRegions.

|
|Description|String|No|0Description| The description of the Internet Shared Bandwidth instance.

 The description must be 2 to 256 characters in length. It must start with a letter, but cannot start with `http://` or `https://`.

 |
|Name|String|No|test123| The name of the Internet Shared Bandwidth instance.

 The name must be 2 to 128 characters in length and can contain letters, numbers, periods \(.\), underscores \(\_\), or hyphens \(-\). The name must start with a letter, but cannot start with `http://` or `https://`.

 |

## Response parameters {#section_ugs_f1g_cz .section}

|Parameter|Type|Example value|Description|
|:--------|:---|-------------|:----------|
|RequestId|String|B450CAD8-50BC-4506-ADA7-35C6CE63E96B|The ID of the request.|

## Examples {#section_ix5_h1g_cz .section}

**Request example**

``` {#ModifyVpnGatewayAttribute1}

https://vpc.aliyuncs.com/?BandwidthPackageId=cbwp-2ze2ic1xd2qeqk145pn4u
&RegionId=cn-hangzhou
&<CommonParameters>

```

**Response example**

XML format

```
<ModifyCommonBandwidthPackageAttributeResponse>
  <RequestId>B450CAD8-50BC-4506-ADA7-35C6CE63E96B</RequestId>
</ModifyCommonBandwidthPackageAttributeResponse>

```

JSON format

```
{
	"RequestId":"B450CAD8-50BC-4506-ADA7-35C6CE63E96B6"
}
```

## Error codes {#section_sml_bnf_xgb .section}

|HTTP status code|Error code|Error message|Description|
|----------------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The specified region ID does not exist.|
|404|InvalidBandwidthPackageId.NotFound|The specified bandwidthPackageId does not exist in our records.|The specified Internet Shared Bandwidth does not exist.|
|400|InvalidParameter.Name.Malformed|The specified Name is not valid.|The name is invalid.|
|400|InvalidParameter.Description.Malformed|The specified Description is not valid.|The description is invalid.|

[See common error codes](https://error-center.aliyun.com/status/product/Vpc)

