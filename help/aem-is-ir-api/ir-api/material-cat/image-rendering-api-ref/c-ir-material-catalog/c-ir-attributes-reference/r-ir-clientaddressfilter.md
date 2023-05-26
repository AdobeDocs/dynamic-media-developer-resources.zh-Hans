---
title: Clientaddresfilter
description: 客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# Clientaddresfilter{#clientaddressfilter}

客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。

指定后，将拒绝从未列出的IP地址上的客户端对此图像目录发起的请求。 `localhost` 始终隐式是 `ClientAddressFilter` 定义（即使未明确指定）。 请求源自 `localhost` 不会被拒绝，无论 `ClientAddressFilter` 规范。

## 属性 {#section-21a2992f108d42fb8660c0d65aa61e13}

使用可选网络掩码([CIDR表示法](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) （已使用）：

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* 中的IP地址 *[!DNL ddd.ddd.ddd.ddd]* 格式

* *[!DNL netmask]* 网络掩码(0...32)

当具有的预处理规则时，此属性被忽略 `<addressfilter>` 个元素。

## 默认 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

继承自 `default::AddressFilter` 如果未定义或为空。

## 示例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* 无访问限制： `0.0.0.0/0`
* 授予对所有地址的访问权限，其开头为 `192: 192.0.0.0/8`
* 授予对512台主机(地址介于 `192.168.12.0` 和 `192.168.13.255: 192.168.12.0/23`

* 授予对单个IP地址的访问权限： `192.168.2.117` 或 `192.168.2.117/32`

## 另请参阅 {#section-6198780c7b3045aabd211eefb38bc565}

[地址过滤器](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
