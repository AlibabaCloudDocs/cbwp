# ModifyCommonBandwidthPackageSpec {#doc_api_951878 .reference}

调用ModifyCommonBandwidthPackageSpec接口更改共享带宽的带宽峰值。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Vpc&api=ModifyCommonBandwidthPackageSpec)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
| Action |String|是|ModifyCommonBandwidthPackageSpec| 要执行的操作。 取值：

  **ModifyCommonBandwidthPackageSpec** 。

 |
| Bandwidth |String|是|100| 共享带宽实例的带宽峰值，单位为Mbps。

 |
| BandwidthPackageId |String|是|cbwp-2ze2ic1xd2qeqk145pn4u| 共享带宽实例的ID。

 |
| RegionId |String|是|cn-hangzhou| 共享带宽实例所在的地域。

 您可以通过调用 [DescribeRegions](~~36063~~) 接口获取地域ID。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|7F129000-F929-4AF5-BE8D-BAE434C795306| 请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

https://vpc.aliyuncs.com/?Action=ModifyCommonBandwidthPackageSpec
&Bandwidth=100
&BandwidthPackageId=cbwp-2ze2ic1xd2qeqk145pn4u
&RegionId=cn-hangzhou
&<公共请求参数>

```

正常返回示例

 `XML` 格式

``` {#xml_return_success_demo}
<ModifyCommonBandwidthPackageSpecResponse>
  <RequestId>7F129000-F929-4AF5-BE8D-BAE434C79530</RequestId>
</ModifyCommonBandwidthPackageSpecResponse>

```

 `JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"7F129000-F929-4AF5-BE8D-BAE434C795306"
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|指定的 RegionId 不存在，请您检查此产品在该地域是否可用。|
|404|InvalidBandwidth.ValueNotSupported|The specified value of Bandwidth not supported.|指定的带宽峰值不支持。|
|404|BandwidthPackage.FinancialLocked|The specified BandwidthPackage has been Financail Lock.|该带宽包被欠费锁定。|

 [查看本产品错误码](https://error-center.aliyun.com/status/product/Vpc) 

