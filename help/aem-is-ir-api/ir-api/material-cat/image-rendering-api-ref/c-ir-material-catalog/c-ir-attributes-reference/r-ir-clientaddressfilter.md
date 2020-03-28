---
description: 客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。
seo-description: 客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Scene7 Image Serving - Image Rendering API
uuid: b68f527b-7fa7-43e3-9517-57a6c3700b06
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# ClientAddressFilter{#clientaddressfilter}

客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。

如果指定，则从未列出IP地址的客户端发出的对此图像目录的请求将被拒绝。 `localhost` 始终隐式地包含在定 `ClientAddressFilter` 义中，即使未显式指定也是如此。 始发自的请 `localhost` 求不会被拒绝，而不管规范如 `ClientAddressFilter` 何。

## 属性 {#section-21a2992f108d42fb8660c0d65aa61e13}

以逗号分隔的IP地址列表(使用[CIDR表示法](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) )可选网络掩码：

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* 格式化的IP地 *[!DNL ddd.ddd.ddd.ddd]* 址

* *[!DNL netmask]* 网络掩码(0...32)

当应用具有元素的预处理规则时，忽略 `<addressfilter>` 此属性。

## 默认 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

如果未定义 `default::AddressFilter` 或为空，则从中继承。

## 示例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* 无访问限制： `0.0.0.0/0`
* 授予对所有地址的访问权限，以 `192: 192.0.0.0/8`
* 授予对512台主机的访问权限，地址位于和之 `192.168.12.0` 间 `192.168.13.255: 192.168.12.0/23`

* 授予对单个IP地址的访问权限： `192.168.2.117` or `192.168.2.117/32`

## 另请参阅 {#section-6198780c7b3045aabd211eefb38bc565}

[地址过滤器](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
