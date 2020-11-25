# ModifyCommonBandwidthPackageSpec

调用ModifyCommonBandwidthPackageSpec接口修改共享带宽的带宽峰值。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Vpc&api=ModifyCommonBandwidthPackageSpec&type=RPC&version=2016-04-28)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyCommonBandwidthPackageSpec|要执行的操作，取值： **ModifyCommonBandwidthPackageSpec**。 |
|Bandwidth|String|是|100|共享带宽实例的带宽峰值，单位为Mbps。 |
|BandwidthPackageId|String|是|cbwp-2ze2ic1xd2qeqk145\*\*\*\*|共享带宽实例的ID。 |
|RegionId|String|是|cn-hangzhou|共享带宽实例所在的地域。

 您可以通过调用[DescribeRegions](~~36063~~)接口获取地域ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|7F129000-F929-4AF5-BE8D-BAE434C795306|请求ID。 |

## 示例

请求示例

```

https://vpc.aliyuncs.com/?Action=ModifyCommonBandwidthPackageSpec
&Bandwidth=100
&BandwidthPackageId=cbwp-2ze2ic1xd2qeqk145****
&RegionId=cn-hangzhou
&<公共请求参数>

```

正常返回示例

`XML` 格式

```
<ModifyCommonBandwidthPackageSpecResponse>
      <RequestId>7F129000-F929-4AF5-BE8D-BAE434C79530</RequestId>
</ModifyCommonBandwidthPackageSpecResponse>
```

`JSON` 格式

```
{
	"RequestId":"7F129000-F929-4AF5-BE8D-BAE434C795306"
}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|指定的 RegionId 不存在，请您检查此产品在该地域是否可用。|
|404|InvalidBandwidth.ValueNotSupported|The specified value of Bandwidth not supported.|指定的带宽峰值不支持。|
|404|BandwidthPackage.FinancialLocked|The specified BandwidthPackage has been Financail Lock.|该带宽包被欠费锁定。|

访问[错误中心](https://error-center.aliyun.com/status/product/Vpc)查看更多错误码。

