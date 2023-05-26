---
description: 客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。
solution: Experience Manager
title: Clientaddresfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# Clientaddresfilter{#clientaddressfilter}

客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。

指定后，会拒绝从未列出的IP地址上的客户端对此图像目录发起的请求。

## 属性 {#section-d785265988324af68835410c9ba54147}

使用可选网络掩码（使用CIDR表示法）的IP地址的逗号分隔列表：

`*`ip地址`*` `[`/ *`netmask`*`]`&#42; `[`，*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ip地址</span> </p> </td> 
  <td class="stentry"> <p>中的IP地址 <span class="varname"> ddd.ddd.ddd.ddd</span> 格式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 网络掩码</span> </p></td> 
  <td class="stentry"> <p>网络掩码(0...32)。 </p></td> 
 </tr> 
</table>

当具有的预处理规则被忽略时，此属性被忽略 `<addressfilter>` 个元素。

## 默认 {#section-de26e8c9225745e985e4beac1f03f4f6}

继承自 `default::AddressFilter` 如果未定义或为空。

## 示例 {#section-a955314d2b6a4213a16c12a8b18d8627}

无访问限制： `0.0.0.0/0`

授予对以192开头的所有地址的访问权限： `192.0.0.0/8`

授予对地址介于192.168.12.0和192.168.13.255之间的512台主机的访问权限： `192.168.12.0/23`

授予对单个IP地址的访问权限： `192.168.2.117` 或 `192.168.2.117/32`

## 另请参阅 {#section-4ea89a7d82e14a4a800487d2d8801465}

[地址过滤器](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
