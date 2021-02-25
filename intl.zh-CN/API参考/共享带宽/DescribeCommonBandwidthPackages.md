# DescribeCommonBandwidthPackages

调用DescribeCommonBandwidthPackages接口查询指定地域中共享带宽实例列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Vpc&api=DescribeCommonBandwidthPackages&type=RPC&version=2016-04-28)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeCommonBandwidthPackages|要执行的操作。 取值：

 **DescribeCommonBandwidthPackages**。 |
|RegionId|String|是|cn-hangzhou|共享带宽所在的地域ID。

 您可以通过调用[DescribeRegions](~~36063~~)接口获取地域ID。 |
|IncludeReservationData|Boolean|否|false|是否包含未生效的订购数据。取值：

 -   **false**（默认值）：不包含。
-   **true**：包含。 |
|BandwidthPackageId|String|否|cbwp-2ze2ic1xd2qeqk145\*\*\*\*|共享带宽实例的ID。 |
|ResourceGroupId|String|否|rg-acfmxazb4ph\*\*\*\*|资源组ID。 |
|Name|String|否|test123|共享带宽实例名称。 |
|PageNumber|Integer|否|1|列表的页码，默认值为**1**。 |
|PageSize|Integer|否|10|分页查询时每页的行数，最大值为**50**，默认值为**10**。 |
|DryRun|Boolean|否|false|是否只预检此次请求。取值范围：

 -   **true**：发送检查请求，不会启动实例。检查项包括是否填写了必需参数、请求格式、实例状态。如果检查不通过，则返回对应错误。如果检查通过，则返回`DRYRUN.SUCCESS`。
-   **false**（默认值）：发送正常请求，通过检查后直接启动实例。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|CommonBandwidthPackages|Array of CommonBandwidthPackage| |共享带宽的详细信息。 |
|CommonBandwidthPackage| | | |
|BandwidthPackageId|String|cbwp-bp1t3sm1ffzmshdki\*\*\*\*|共享带宽的ID。 |
|Name|String|abc|共享带宽的名称。 |
|Description|String|none|共享带宽的描述信息。 |
|Bandwidth|String|20|共享带宽的带宽峰值。 单位：Mbps。 |
|InternetChargeType|String|PayByBandwidth|共享带宽的计费方式。

 -   **PayBy95**：按增强型95计费。
-   **PayByBandwidth**：按带宽计费。 |
|Ratio|Integer|100|比率。 |
|RegionId|String|cn-hangzhou|共享带宽实例的地域ID。 |
|CreationTime|String|2017-06-28T06:39:20Z|共享带宽实例创建的时间。 |
|InstanceChargeType|String|PostPaid|共享带宽实例的计费类型。 |
|BusinessStatus|String|Normal|共享带宽实例的状态。

 -   **Normal**：正常状态。
-   **FinancialLocked**：欠费。
-   **Unactivated**：未激活。 |
|PublicIpAddresses|Array of PublicIpAddresse| |共享带宽实例中的公网IP地址。 |
|PublicIpAddresse| | | |
|IpAddress|String|116.XX.XX.250|公网IP地址。 |
|AllocationId|String|eip-bp13e9i2qst4g6jzi\*\*\*\*|公网IP的实例ID。 |
|BandwidthPackageIpRelationStatus|String|BINDED|共享带宽和EIP的关联状态。取值：

 -   **BINDED**：EIP与共享带宽关联完成。
-   **BINDING**：关联中。 |
|DeletionProtection|Boolean|true|是否开启删除保护：

 -   **true**：开启。
-   **false**：关闭。 |
|ExpiredTime|String|2019-01-15T03:08:37Z|共享带宽实例的过期时间。 |
|HasReservationData|String|false|是否有待生效的订单。

 -   **false**：没有待生效的订单。
-   **true**：有待生效的订单。 |
|ISP|String|BGP|服务提供商，大部分是BGP。 |
|ReservationActiveTime|String|2018-08-30T16:00Z|续费生效时间。 |
|ReservationBandwidth|String|10|变配之后的带宽值。 |
|ReservationInternetChargeType|String|PayByBandwidth|变配之后的计费方式。 |
|ReservationOrderType|String|RENEWCHANGE|续费变配方式。

 -   **RENEWCHANGE**：续费变配。
-   **TEMP\_UPGRADE**：短时升配。
-   **UPGRADE**：升级。 |
|ResourceGroupId|String|rg-acfmxazb4ph\*\*\*\*|资源组ID。 |
|ServiceManaged|Integer|1|是否为服务账号创建的资源。取值：

 -   **0**：非服务账号创建。
-   **1**：服务账号创建。 |
|Status|String|Available|共享带宽实例的状态。默认取值：**Available**。 |
|TotalCount|Integer|1|列表条条目数。 |
|PageNumber|Integer|1|当前页码。 |
|PageSize|Integer|10|每页包含多少条目。 |
|RequestId|String|20E6FD1C-7321-4DAD-BDFD-EC8769E4AA33|请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeCommonBandwidthPackages
&RegionId=cn-hangzhou
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<DescribeCommonBandwidthPackagesResponse>
  <TotalCount>1</TotalCount>
  <PageSize>10</PageSize>
  <RequestId>20E6FD1C-7321-4DAD-BDFD-EC8769E4AA33</RequestId>
  <PageNumber>1</PageNumber>
  <CommonBandwidthPackages>
        <CommonBandwidthPackage>
              <Status>Available</Status>
              <Description>none</Description>
              <ServiceManaged>1</ServiceManaged>
              <ResourceGroupId>rg-acfmxazb4ph****</ResourceGroupId>
              <InstanceChargeType>PostPaid</InstanceChargeType>
              <ISP>BGP</ISP>
              <HasReservationData>false</HasReservationData>
              <DeletionProtection>true</DeletionProtection>
              <BusinessStatus>Normal</BusinessStatus>
              <ReservationInternetChargeType>PayByBandwidth</ReservationInternetChargeType>
              <InternetChargeType>PayByBandwidth</InternetChargeType>
              <Name>abc</Name>
              <ReservationOrderType>RENEWCHANGE</ReservationOrderType>
              <ExpiredTime>2019-01-15T03:08:37Z</ExpiredTime>
              <Bandwidth>20</Bandwidth>
              <CreationTime>2017-06-28T06:39:20Z</CreationTime>
              <BandwidthPackageId>cbwp-bp1t3sm1ffzmshdki****</BandwidthPackageId>
              <Ratio>100</Ratio>
              <RegionId>cn-hangzhou</RegionId>
              <ReservationActiveTime>2018-08-30T16:00Z</ReservationActiveTime>
              <ReservationBandwidth>10</ReservationBandwidth>
              <PublicIpAddresses>
                    <PublicIpAddresse>
                          <AllocationId>eip-bp13e9i2qst4g6jzi****</AllocationId>
                          <BandwidthPackageIpRelationStatus>BINDED</BandwidthPackageIpRelationStatus>
                          <IpAddress>116.XX.XX.250</IpAddress>
                    </PublicIpAddresse>
              </PublicIpAddresses>
        </CommonBandwidthPackage>
  </CommonBandwidthPackages>
</DescribeCommonBandwidthPackagesResponse>
```

`JSON`格式

```
{"TotalCount":"1","PageSize":"10","RequestId":"20E6FD1C-7321-4DAD-BDFD-EC8769E4AA33","PageNumber":"1","CommonBandwidthPackages":{"CommonBandwidthPackage":[{"Status":"Available","Description":"none","ServiceManaged":"1","ResourceGroupId":"rg-acfmxazb4ph****","InstanceChargeType":"PostPaid","ISP":"BGP","HasReservationData":"false","DeletionProtection":"true","BusinessStatus":"Normal","ReservationInternetChargeType":"PayByBandwidth","InternetChargeType":"PayByBandwidth","Name":"abc","ReservationOrderType":"RENEWCHANGE","ExpiredTime":"2019-01-15T03:08:37Z","Bandwidth":"20","CreationTime":"2017-06-28T06:39:20Z","BandwidthPackageId":"cbwp-bp1t3sm1ffzmshdki****","Ratio":"100","RegionId":"cn-hangzhou","ReservationActiveTime":"2018-08-30T16:00Z","ReservationBandwidth":"10","PublicIpAddresses":{"PublicIpAddresse":[{"AllocationId":"eip-bp13e9i2qst4g6jzi****","BandwidthPackageIpRelationStatus":"BINDED","IpAddress":"116.XX.XX.250"}]}}]}}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|指定的 RegionId 不存在，请您检查此产品在该地域是否可用。|
|400|InvalidBandwidthPackageIdNumber.NotSupported|The number of BandwidthPackageIds exceeds the limit.|共享带宽包的数量超过Quota限制。|
|400|InvalidResourceGroupId|The specified ResourceGroupId does not exist.|资源组ID不存在。|
|400|OperationUnsupported.ResourceGroupId|ResourceGroup is not supported in this region.|资源组功能未打开。|

访问[错误中心](https://error-center.alibabacloud.com/status/product/Vpc)查看更多错误码。

