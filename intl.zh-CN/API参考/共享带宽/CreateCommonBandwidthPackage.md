# CreateCommonBandwidthPackage

调用CreateCommonBandwidthPackage接口创建共享带宽实例。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Vpc&api=CreateCommonBandwidthPackage&type=RPC&version=2016-04-28)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateCommonBandwidthPackage|要执行的操作，取值：**CreateCommonBandwidthPackage**。 |
|Bandwidth|Integer|是|5|共享带宽的带宽峰值，取值：

 **1**~**1000**。

 单位为Mbps。 |
|RegionId|String|是|cn-hangzhou|共享带宽所在的地域ID。您可以通过调用[DescribeRegions](~~36063~~)接口获取地域ID。 |
|Zone|String|否|cn-hangzhou-a|共享带宽的可用区。

 不需要传入该参数。 |
|ISP|String|否|BGP|线路类型，取值：

 -   **BGP**：BGP（多线）线路。
-   **BGP\_PRO**：BGP（多线）精品线路。

 **说明：**

-   目前，全部地域都支持BGP（多线）线路共享带宽，仅中国（香港）地域支持BGP（多线）精品线路共享带宽。
-   如果是开通了单线带宽白名单的用户，ISP字段可以设置为**ChinaTelecom**（中国电信）、**ChinaUnicom**（中国联通）和**ChinaMobile**（中国移动）；如果是杭州金融云用户，该字段必填，取值：**BGP\_FinanceCloud**。 |
|Name|String|否|test123|共享带宽的名称。

 长度为2~128个字符，必须以字母或中文开头，可包含数字、半角句点（.）、下划线（\_）和短划线（-），但不能以`http://`或`https://`开头。 |
|Description|String|否|abc|共享带宽的描述信息。

 长度为2~256个字符，必须以字母或中文开头，但不能以`http://`或`https://`开头。 |
|ClientToken|String|否|02fb3da4-130e-11e9-8e44-001\*\*\*\*|用于保证请求的幂等性。由客户端生成该参数值，要保证在不同请求间唯一，最大值不超过64个ASCII字符。 |
|ResourceGroupId|String|否|rg-acfmxazdjdhd\*\*\*\*|资源组ID。 |
|Ratio|Integer|否|20|共享带宽的保底百分比，取值为**20**，即保底百分比的范围是20%。

 **说明：** 仅中国站支持此参数。 |
|InternetChargeType|String|否|中国站示例值：PayByBandwidth，国际站示例值：PayByTraffic|共享带宽的计费方式，取值：**PayByTraffic**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|BandwidthPackageId|String|cbwp-bp1vevu8h3ieh\*\*\*\*|共享带宽实例的ID。 |
|RequestId|String|FF39F653-033E-4CD9-9EDF-3CCA5A71FBC3|请求ID。 |
|ResourceGroupId|String|rg-acfmxazdjdhd\*\*\*\*|资源组ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateCommonBandwidthPackage
&Bandwidth=5
&RegionId=cn-hangzhou
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<CreateCommonBandwidthPackageResponse>
      <BandwidthPackageId>cbwp-bp1vevu8h3iehdfradfra****</BandwidthPackageId>
      <ResourceGroupId>rg-acfmxazdjdhd****</ResourceGroupId>
      <RequestId>FF39F653-033E-4CD9-9EDF-3CCA5A71FBC3</RequestId>
</CreateCommonBandwidthPackageResponse>
```

`JSON`格式

```
{"ResourceGroupId":"rg-acfmxazdjdhd****","RequestId":"FF39F653-033E-4CD9-9EDF-3CCA5A71FBC3","BandwidthPackageId":"cbwp-bp1vevu8h3ieh****"}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|指定的regionid不存在。|
|404|InvalidVpcId.NotFound|Specified value of VpcId is not found in our record.|该 VPC 不存在，请您检查输入的 VPC 是否正确。|
|400|MissingParameter|Miss mandatory parameter.|缺少必要参数，请您检查必填参数是否都已填后再进行操作。|
|404|InvalidZoneId.NotFound|Specified value of ZoneId is not exists.|该可用区不存在。|
|400|InvalidParameter.Name.Malformed|The specified Name is not valid.|该名称不合法，请您按照正确的格式书写名称。|
|400|InvalidParameter.Description.Malformed|The specified Description is not valid.|该描述不合法。|
|400|InvalidResourceGroupId|The specified ResourceGroupId does not exist.|资源组ID不存在。|

访问[错误中心](https://error-center.alibabacloud.com/status/product/Vpc)查看更多错误码。

