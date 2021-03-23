---
description: 客户端IP地址筛选器。 允许指定一个或多个IP地址或地址范围。
seo-description: 客户端IP地址筛选器。 允许指定一个或多个IP地址或地址范围。
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
uuid: b68f527b-7fa7-43e3-9517-57a6c3700b06
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# ClientAddressFilter{#clientaddressfilter}

客户端IP地址筛选器。 允许指定一个或多个IP地址或地址范围。

如果指定，则来自未列出IP地址的客户端的此图像目录请求将被拒绝。 `localhost` 始终隐式部分定义， `ClientAddressFilter` 即使未显式指定也是如此。始自`localhost`的请求从不被拒绝，无论`ClientAddressFilter`规范如何。

## 属性 {#section-21a2992f108d42fb8660c0d65aa61e13}

以逗号分隔的IP地址列表(使用可选网络掩码（[CIDR表示法](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)）：

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* 格式的IP地 *[!DNL ddd.ddd.ddd.ddd]* 址

* *[!DNL netmask]* 网络掩码(0...32)

应用具有`<addressfilter>`元素的预处理规则时，将忽略此属性。

## 默认 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

如果未定义或为空，则从`default::AddressFilter`继承。

## 示例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* 无访问限制：`0.0.0.0/0`
* 授予对以`192: 192.0.0.0/8`开头的所有地址的访问权限
* 授予对地址介于`192.168.12.0`和`192.168.13.255: 192.168.12.0/23`之间的512台主机的访问权限

* 授予对单个IP地址的访问权限：`192.168.2.117`或`192.168.2.117/32`

## 另请参阅 {#section-6198780c7b3045aabd211eefb38bc565}

[地址筛选器](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
