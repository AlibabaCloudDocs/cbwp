# ModifyCommonBandwidthPackageAttribute {#doc_api_920577 .reference}

调用ModifyCommonBandwidthPackageAttribute修改共享带宽实例的名称和描述信息。

## 调试 {#apiExplorer .section}

单击[这里](https://api.aliyun.com/#product=Vpc&api=ModifyCommonBandwidthPackageAttribute)在OpenAPI Explorer中进行可视化调试，并生成SDK代码示例。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
| Action |String|是|ModifyCommonBandwidthPackageAttribute| 要执行的操作。 取值：

  **ModifyCommonBandwidthPackageAttribute** 

 |
| BandwidthPackageId |String|是|cbwp-2ze2ic1xd2qeqk145pn4u| 共享带宽实例的ID。

 |
| RegionId |String|是|cn-hangzhou| 共享带宽所在的地域。

 您可以通过调用 [DescribeRegions](~~36063~~) 接口获取地域ID。

 |
| Description |String|否|描述| 共享带宽的描述信息。 长度为 2-256个字符，必须以字母或中文开头，但不能以 `http://` 或 `https://` 开头。

 |
| Name |String|否|test123| 共享带宽的名称。 长度为 2-128个字符，必须以字母或中文开头，可包含数字，点号（.），下划线（\_）和短横线（-）。但不能以 `http://` 或 `https://` 开头。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|B450CAD8-50BC-4506-ADA7-35C6CE63E96B| 请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

https://vpc.aliyuncs.com/?BandwidthPackageId=cbwp-2ze2ic1xd2qeqk145pn4u
&RegionId=cn-hangzhou
&<公共请求参数>

```

正常返回示例

 `XML` 格式

``` {#xml_return_success_demo}
<ModifyCommonBandwidthPackageAttributeResponse>
  <RequestId>B450CAD8-50BC-4506-ADA7-35C6CE63E96B</RequestId>
</ModifyCommonBandwidthPackageAttributeResponse>

```

 `JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"B450CAD8-50BC-4506-ADA7-35C6CE63E96B6"
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|指定的 RegionId 不存在，请您检查此产品在该地域是否可用。|
|404|InvalidBandwidthPackageId.NotFound|The specified bandwidthPackageId does not exist in our records.|该共享带宽包不存在，请您检查输入参数是否正确。|
|400|InvalidParameter.Name.Malformed|The specified Name is not valid.|该名称不合法，请您按照正确的格式书写名称。|
|400|InvalidParameter.Description.Malformed|The specified Description is not valid.|该描述不合法。|

 [查看本产品错误码](https://error-center.aliyun.com/status/product/Vpc) 

