# ModifyCommonBandwidthPackageAttribute

调用ModifyCommonBandwidthPackageAttribute修改共享带宽实例的名称和描述信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Vpc&api=ModifyCommonBandwidthPackageAttribute&type=RPC&version=2016-04-28)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyCommonBandwidthPackageAttribute|要执行的操作。 取值：

 **ModifyCommonBandwidthPackageAttribute** |
|BandwidthPackageId|String|是|cbwp-2ze2ic1xd2qeqk145\*\*\*\*|共享带宽实例的ID。 |
|RegionId|String|是|cn-hangzhou|共享带宽所在的地域。

 您可以通过调用[DescribeRegions](~~36063~~)接口获取地域ID。 |
|Name|String|否|test123|共享带宽的名称。 长度为 2~128个字符，必须以字母或中文开头，可包含数字，半角句点（.），下划线（\_）和短划线（-）。但不能以`http://` 或`https://`开头。 |
|Description|String|否|描述|共享带宽的描述信息。 长度为 2~256个字符，必须以字母或中文开头，但不能以`http://`或`https://`开头。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|B450CAD8-50BC-4506-ADA7-35C6CE63E96B|请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ModifyCommonBandwidthPackageAttribute
&BandwidthPackageId=cbwp-2ze2ic1xd2qeqk145****
&RegionId=cn-hangzhou
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ModifyCommonBandwidthPackageAttributeResponse>
      <RequestId>B450CAD8-50BC-4506-ADA7-35C6CE63E96B</RequestId>
</ModifyCommonBandwidthPackageAttributeResponse>
```

`JSON`格式

```
{
    "RequestId":"B450CAD8-50BC-4506-ADA7-35C6CE63E96B6"
}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|指定的 RegionId 不存在，请您检查此产品在该地域是否可用。|
|404|InvalidBandwidthPackageId.NotFound|The specified bandwidthPackageId does not exist in our records.|该共享带宽包不存在，请您检查输入参数是否正确。|
|400|InvalidParameter.Name.Malformed|The specified Name is not valid.|该名称不合法，请您按照正确的格式书写名称。|
|400|InvalidParameter.Description.Malformed|The specified Description is not valid.|该描述不合法。|

访问[错误中心](https://error-center.aliyun.com/status/product/Vpc)查看更多错误码。

