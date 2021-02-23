# AddCommonBandwidthPackageIp

调用AddCommonBandwidthPackageIp接口添加EIP到共享带宽中。

## API描述

调用本接口添加EIP时，请注意：

-   只支持添加按量计费的EIP。
-   EIP和共享带宽的地域必须相同。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Vpc&api=AddCommonBandwidthPackageIp&type=RPC&version=2016-04-28)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|AddCommonBandwidthPackageIp|要执行的操作，取值：**AddCommonBandwidthPackageIp**。 |
|BandwidthPackageId|String|是|cbwp-2ze2ic1xd2qeqasdf\*\*\*\*|共享带宽的ID。 |
|IpInstanceId|String|是|eip-2zeerraiwb7uqwed\*\*\*\*|EIP实例的ID。

 您可以通过调用[DescribeEipAddresses](~~36018~~)接口查询EIP实例的ID。 |
|RegionId|String|是|cn-hangzhou|共享带宽所在的地域ID。

 您可以通过调用[DescribeRegions](~~36063~~)接口获取地域ID。 |
|IpType|String|否|EIP|IP类型。取值：**EIP**，表示将EIP添加至共享带宽。 |
|ClientToken|String|否|0c593ea1-3bea-11e9-b96b-88e9fe637760|保证请求幂等性。从您的客户端生成一个参数值，确保不同请求间该参数值唯一。ClientToken只支持ASCII字符，且不能超过64个字符。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|01FDDD49-C4B7-4D2A-A8E5-A93915C450A6|请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=AddCommonBandwidthPackageIp
&BandwidthPackageId=cbwp-2ze2ic1xd2qeqasdf****
&IpInstanceId=eip-2zeerraiwb7uqwed****
&RegionId=cn-hangzhou
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<AddCommonBandwidthPackageIpResponse>
      <RequestId>01FDDD49-C4B7-4D2A-A8E5-A93915C450A6</RequestId>
</AddCommonBandwidthPackageIpResponse>
```

`JSON`格式

```
{
    "RequestId": "01FDDD49-C4B7-4D2A-A8E5-A93915C450A6"
}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|指定的 RegionId 不存在，请您检查此产品在该地域是否可用。|
|404|InvalidBandwidthPackageId.NotFound|The specified bandwidthPackageId does not exist in our records.|该共享带宽包不存在，请您检查输入参数是否正确。|
|400|InvalidInstanceId.NotFound|The InstanceId is not found.|实例InstanceId找不到。|

访问[错误中心](https://error-center.alibabacloud.com/status/product/Vpc)查看更多错误码。

