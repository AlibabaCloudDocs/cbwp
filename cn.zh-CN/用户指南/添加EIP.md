# 添加EIP {#task_hjr_jlk_z2b .task}

创建共享带宽实例后，您需要将使用该共享带宽的EIP添加到共享带宽实例中。

添加EIP前，您必须了解：

-   添加EIP到共享带宽实例后，EIP原本的带宽峰值无效，与共享带宽实例的带宽峰值相同。
-   添加EIP到共享带宽实例后，EIP原本的计费模式无效。EIP变为一个公网IP，不额外收取EIP的流量费，但正常收取EIP的实例费。
-   EIP的实例费与其是否加入共享带宽无关，当EIP绑定至专有网络类型ECS实例后，将免除EIP实例费；而绑定至NAT网关、SLB实例、辅助弹性网卡和高可用虚拟IP时，仍正常收取EIP实例费。
-   单个共享带宽实例最多可添加100个EIP。如需添加更多EIP，请[提交工单](https://workorder-intl.console.aliyun.com/?spm=5176.11182188.console-base-top.dworkorder.18ae4882n3v6ZW#/ticket/createIndex)。
-   共享带宽实例会自动移出欠费的EIP。共享带宽实例欠费后，系统会自动移出所有添加到共享带宽实例的EIP。

1.  登录[专有网络管理控制台](https://vpcnext.console.aliyun.com)。
2.  在左侧导航栏，单击**共享带宽**。
3.  选择共享带宽实例的地域。
4.  在共享带宽页面，找到目标共享带宽实例，单击**操作**列下的**添加IP**。
5.  在添加IP页面，根据以下信息添加EIP，然后单击**确定**。 
    -   如果您在该地域下没有可用的EIP，单击**购买EIP并添加到带宽包**，然后输入购买EIP的个数。

        系统会自动创建指定个数的按流量计费的按量计费EIP并添加到共享带宽实例中。

    -   如果您在该地域下有可用的EIP，单击**从已有EIP列表选取**，然后在**可用EIP列表**中选择要添加的EIP。

        ![添加EIP](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/19039/156878883511049_zh-CN.png)


**相关文档**  


[AddCommonBandwidthPackageIp](../../../../intl.zh-CN/API参考/共享带宽/AddCommonBandwidthPackageIp.md#)

