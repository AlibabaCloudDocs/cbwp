# DescribeCommonBandwidthPackages

Queries EIP bandwidth plans in a region.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Vpc&api=DescribeCommonBandwidthPackages&type=RPC&version=2016-04-28)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeCommonBandwidthPackages|The operation that you want to perform. Set the value to

 **DescribeCommonBandwidthPackages**. |
|RegionId|String|Yes|cn-hangzhou|The ID of the region where the EIP bandwidth plan is created.

 You can call the [DescribeRegions](~~36063~~) operation to query region IDs. |
|IncludeReservationData|Boolean|No|false|Specifies whether to return data of orders that have not taken effect. Valid values:

 -   **false**: no. This is the default value.
-   **true**: yes. |
|BandwidthPackageId|String|No|cbwp-2ze2ic1xd2qeqk145\*\*\*\*|The ID of the EIP bandwidth plan. |
|ResourceGroupId|String|No|rg-acfmxazb4ph\*\*\*\*|The ID of the resource group. |
|Name|String|No|test123|The name of the EIP bandwidth plan. |
|PageNumber|Integer|No|1|The number of the page to return. Default value: **1**. |
|PageSize|Integer|No|10|The number of entries to return on each page. Maximum value: **50**. Default value: **10**. |
|DryRun|Boolean|No|false|Specifies whether to precheck only the request. Valid values:

 -   **true**: prechecks the request without performing the operation. Check items include the request format, instance status, and whether the required parameters are specified. An error message is returned if the request fails the precheck. If the request passes the precheck, `DRYRUN.SUCCESS` is returned.
-   **false**: prechecks the request. After the request passes the precheck, the operation is performed. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|CommonBandwidthPackages|Array of CommonBandwidthPackage| |The details of the EIP bandwidth plan. |
|CommonBandwidthPackage| | | |
|BandwidthPackageId|String|cbwp-bp1t3sm1ffzmshdki\*\*\*\*|The ID of the EIP bandwidth plan. |
|Name|String|abc|The name of the EIP bandwidth plan. |
|Description|String|none|The description of the EIP bandwidth plan. |
|Bandwidth|String|20|The maximum bandwidth of the EIP bandwidth plan. Unit: Mbit/s. |
|InternetChargeType|String|PayByBandwidth|The billing method of the billing method. Valid values:

 -   **PayBy95**: enhanced 95th percentile
-   **PayByBandwidth**: pay-by-bandwidth |
|Ratio|Integer|100|The ratio. |
|RegionId|String|cn-hangzhou|The ID of the region to which the EIP bandwidth plan belongs. |
|CreationTime|String|2017-06-28T06:39:20Z|The time when the EIP bandwidth plan was created. |
|InstanceChargeType|String|PostPaid|The billing method of the EIP bandwidth plan. |
|BusinessStatus|String|Normal|The state of the EIP bandwidth plan. Valid values:

 -   **Normal**: The EIP bandwidth plan is working as expected.
-   **FinancialLocked**: The EIP bandwidth plan has overdue payments.
-   **Unactivated**: The EIP bandwidth plan is not enabled. |
|PublicIpAddresses|Array of PublicIpAddresse| |The public IP address of the EIP bandwidth plan. |
|PublicIpAddresse| | | |
|IpAddress|String|116.XX.XX.250|The public IP address of the VPN gateway. |
|AllocationId|String|eip-bp13e9i2qst4g6jzi\*\*\*\*|The ID of the public IP address. |
|BandwidthPackageIpRelationStatus|String|BINDED|Indicates whether the EIP bandwidth plan is associated with the EIP. Valid values:

 -   **BINDED**: associated
-   **BINDING**: associating |
|DeletionProtection|Boolean|true|Indicates whether deletion protection is enabled. Valid values:

 -   **true**: yes
-   **false**: no |
|ExpiredTime|String|2019-01-15T03:08:37Z|The time when the EIP bandwidth plan expires. |
|HasReservationData|String|false|Indicates whether a pending order exists. Valid values:

 -   **false**: no
-   **true**: yes |
|ISP|String|BGP|The service provider. In most cases, the value is BGP. |
|ReservationActiveTime|String|2018-08-30T16:00Z|The time when the renewal takes effect. |
|ReservationBandwidth|String|10|The bandwidth value after you modify the specification of the EIP bandwidth plan. |
|ReservationInternetChargeType|String|PayByBandwidth|The billing method after you modify the specification of the EIP bandwidth plan. |
|ReservationOrderType|String|RENEWCHANGE|The method of the specification modification and renewal. Valid values:

 -   **RENEWCHANGE**: renewal and specification modification
-   **TEMP\_UPGRADE**: temporary upgrade
-   **UPGRADE**: upgrade |
|ResourceGroupId|String|rg-acfmxazb4ph\*\*\*\*|The ID of the resource group. |
|ServiceManaged|Integer|1|Indicates whether the resource is created by the service account. Valid values:

 -   **0**: no
-   **1**: yes |
|Status|String|Available|The state of the EIP bandwidth plan. Default value: **Available**. |
|TotalCount|Integer|1|The number of entries returned. |
|PageNumber|Integer|1|The page number of the returned page. |
|PageSize|Integer|10|The number of entries returned per page. |
|RequestId|String|20E6FD1C-7321-4DAD-BDFD-EC8769E4AA33|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeCommonBandwidthPackages
&RegionId=cn-hangzhou
&<Common request parameters>
```

Sample success responses

`XML` format

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

`JSON` format

```
{"TotalCount":"1","PageSize":"10","RequestId":"20E6FD1C-7321-4DAD-BDFD-EC8769E4AA33","PageNumber":"1","CommonBandwidthPackages":{"CommonBandwidthPackage":[{"Status":"Available","Description":"none","ServiceManaged":"1","ResourceGroupId":"rg-acfmxazb4ph****","InstanceChargeType":"PostPaid","ISP":"BGP","HasReservationData":"false","DeletionProtection":"true","BusinessStatus":"Normal","ReservationInternetChargeType":"PayByBandwidth","InternetChargeType":"PayByBandwidth","Name":"abc","ReservationOrderType":"RENEWCHANGE","ExpiredTime":"2019-01-15T03:08:37Z","Bandwidth":"20","CreationTime":"2017-06-28T06:39:20Z","BandwidthPackageId":"cbwp-bp1t3sm1ffzmshdki****","Ratio":"100","RegionId":"cn-hangzhou","ReservationActiveTime":"2018-08-30T16:00Z","ReservationBandwidth":"10","PublicIpAddresses":{"PublicIpAddresse":[{"AllocationId":"eip-bp13e9i2qst4g6jzi****","BandwidthPackageIpRelationStatus":"BINDED","IpAddress":"116.XX.XX.250"}]}}]}}
```

## Error codes

|HttpCode|Error code|Error message|Description|
|--------|----------|-------------|-----------|
|404|InvalidRegionId.NotFound|The specified RegionId does not exist in our records.|The error message returned because the specified region ID does not exist. Check whether the service is available in the region.|
|400|InvalidBandwidthPackageIdNumber.NotSupported|The number of BandwidthPackageIds exceeds the limit.|The error message returned because the number of EIP bandwidth plans has reached the upper limit.|
|400|InvalidResourceGroupId|The specified ResourceGroupId does not exist.|The error message returned because the specified resource group ID does not exist.|
|400|OperationUnsupported.ResourceGroupId|ResourceGroup is not supported in this region.|The error message returned because the resource group feature is not enabled.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Vpc).

