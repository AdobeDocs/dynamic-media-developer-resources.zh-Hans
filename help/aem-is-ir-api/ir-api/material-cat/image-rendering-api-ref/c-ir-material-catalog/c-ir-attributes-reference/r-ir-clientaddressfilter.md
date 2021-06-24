---
description: 客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。

指定后，对此图像目录的请求（源自未列入IP地址的客户端）将被拒绝。 `localhost` 始终隐式地包含在定 `ClientAddressFilter` 义中，即使未明确指定也是如此。无论`ClientAddressFilter`规范如何，始发自`localhost`的请求都永远不会被拒绝。

## 属性 {#section-21a2992f108d42fb8660c0d65aa61e13}

以逗号分隔的IP地址列表(使用可选网络掩码（[CIDR表示法](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)）：

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* 格式化的IP地 *[!DNL ddd.ddd.ddd.ddd]* 址

* *[!DNL netmask]* 网络掩码(0...32)

当应用具有`<addressfilter>`元素的预处理规则时，将忽略此属性。

## 默认 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

从`default::AddressFilter`继承（如果未定义或为空）。

## 示例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* 无访问限制：`0.0.0.0/0`
* 授予对以`192: 192.0.0.0/8`开始的所有地址的访问权限
* 授予对地址介于`192.168.12.0`和`192.168.13.255: 192.168.12.0/23`之间的512台主机的访问权限

* 授予对单个IP地址的访问权限：`192.168.2.117`或`192.168.2.117/32`

## 另请参阅 {#section-6198780c7b3045aabd211eefb38bc565}

[地址筛选器](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
