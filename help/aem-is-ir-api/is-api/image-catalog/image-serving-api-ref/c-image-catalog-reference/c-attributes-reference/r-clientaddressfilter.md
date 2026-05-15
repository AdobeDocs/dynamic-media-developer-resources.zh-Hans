---
description: 客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。
solution: Experience Manager
title: Clientaddresfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
TQID: 'https://experienceleague.adobe.com/cQT0eRo0amqhX76H3dNZakwlGsKt3-MAkIsRZytyREI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 132
ht-degree: 3%

---

# Clientaddresfilter{#clientaddressfilter}

客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。

指定后，从位于未列出的IP地址的客户端发出的对此图像目录的请求将被拒绝。

## 属性 {#section-d785265988324af68835410c9ba54147}

使用可选网络掩码（使用CIDR表示法）的逗号分隔IP地址列表：

`*`ipAddress`*` `[`/ *`netmask`*`]`&#42; `[`，*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p>采用<span class="varname"> ddd.ddd.ddd.ddd</span>格式的IP地址。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">网络掩码</span> </p></td> 
  <td class="stentry"> <p>网络掩码(0...32)。 </p></td> 
 </tr> 
</table>

当应用具有`<addressfilter>`元素的预处理规则时，将忽略此属性。

## 默认 {#section-de26e8c9225745e985e4beac1f03f4f6}

如果未定义或为空，则从`default::AddressFilter`继承。

## 示例 {#section-a955314d2b6a4213a16c12a8b18d8627}

无访问限制：`0.0.0.0/0`

授予对以192开头的所有地址的访问权限： `192.0.0.0/8`

授予对地址介于192.168.12.0和192.168.13.255之间的512台主机的访问权限： `192.168.12.0/23`

授予对单个IP地址的访问权限： `192.168.2.117`或`192.168.2.117/32`

## 另请参阅 {#section-4ea89a7d82e14a4a800487d2d8801465}

[地址过滤器](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
