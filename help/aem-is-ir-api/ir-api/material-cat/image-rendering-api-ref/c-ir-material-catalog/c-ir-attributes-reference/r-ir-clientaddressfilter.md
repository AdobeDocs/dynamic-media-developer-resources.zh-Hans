---
title: Clientaddresfilter
description: 客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# Clientaddresfilter{#clientaddressfilter}

客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。

指定后，将拒绝从未列出的IP地址上的客户端发出的对此图像目录的请求。 `localhost`始终是`ClientAddressFilter`定义的隐式部分，即使未显式指定。 无论是否遵循`localhost`规范，源自`ClientAddressFilter`的请求都不会被拒绝。

## 属性 {#section-21a2992f108d42fb8660c0d65aa61e13}

使用可选netmasks的IP地址逗号分隔列表（使用了[CIDR表示法](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)）：

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]*&#x200B;格式的&#x200B;*[!DNL ddd.ddd.ddd.ddd]* IP地址

* *[!DNL netmask]*&#x200B;网络掩码（0至32）

当应用具有`<addressfilter>`元素的预处理规则时，将忽略此属性。

## 默认 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

如果未定义或为空，则从`default::AddressFilter`继承。

## 示例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* 无访问限制：`0.0.0.0/0`
* 授予对以`192: 192.0.0.0/8`开头的所有地址的访问权限
* 授予对512台地址介于`192.168.12.0`和`192.168.13.255: 192.168.12.0/23`之间的主机的访问权限

* 授予对单个IP地址的访问权限： `192.168.2.117`或`192.168.2.117/32`

## 另请参阅 {#section-6198780c7b3045aabd211eefb38bc565}

[地址过滤器](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
