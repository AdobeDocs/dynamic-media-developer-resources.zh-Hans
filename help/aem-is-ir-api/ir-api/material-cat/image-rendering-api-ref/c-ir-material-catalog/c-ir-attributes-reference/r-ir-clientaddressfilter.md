---
title: Clientaddresfilter
description: 客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
TQID: 'https://experienceleague.adobe.com/azMITpRcITTOEB0FCev6vWiTmocumP-0HTQD3rIV-fA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 156
ht-degree: 2%

---

# Clientaddresfilter{#clientaddressfilter}

客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。

指定后，将拒绝从未列出的IP地址上的客户端发出的对此图像目录的请求。 `localhost`始终是`ClientAddressFilter`定义的隐式部分，即使未显式指定。 无论是否遵循`ClientAddressFilter`规范，源自`localhost`的请求都不会被拒绝。

## 属性 {#section-21a2992f108d42fb8660c0d65aa61e13}

使用可选netmasks的IP地址逗号分隔列表（使用了[CIDR表示法](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)）：

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ddd.ddd.ddd.ddd]*&#x200B;格式的&#x200B;*[!DNL ipAddress]* IP地址

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
