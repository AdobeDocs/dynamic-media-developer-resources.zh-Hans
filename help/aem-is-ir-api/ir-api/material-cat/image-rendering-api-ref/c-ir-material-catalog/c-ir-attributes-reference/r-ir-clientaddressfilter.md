---
title: ClientAddressFilter
description: 客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。

指定后，对此图像目录的请求将被拒绝，这些请求源自位于未列出的IP地址的客户端。 `localhost` 始终隐式包含在 `ClientAddressFilter` 定义，即使未明确指定也是如此。 来自 `localhost` 不会被拒绝，无论 `ClientAddressFilter` 规范。

## 属性 {#section-21a2992f108d42fb8660c0d65aa61e13}

带有可选网络掩码的IP地址列表（以逗号分隔）[CIDR表示法](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) 使用):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* 中的IP地址 *[!DNL ddd.ddd.ddd.ddd]* 格式

* *[!DNL netmask]* 网络掩码(0...32)

当具有 `<addressfilter>` 元素。

## 默认 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

继承自 `default::AddressFilter` 如果未定义或为空。

## 示例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* 无访问限制： `0.0.0.0/0`
* 授予对所有地址的访问权限(以 `192: 192.0.0.0/8`
* 授予对512台主机的访问权限，这些主机的地址介于 `192.168.12.0` 和 `192.168.13.255: 192.168.12.0/23`

* 授予对单个IP地址的访问权限： `192.168.2.117` 或 `192.168.2.117/32`

## 另请参阅 {#section-6198780c7b3045aabd211eefb38bc565}

[地址筛选器](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
