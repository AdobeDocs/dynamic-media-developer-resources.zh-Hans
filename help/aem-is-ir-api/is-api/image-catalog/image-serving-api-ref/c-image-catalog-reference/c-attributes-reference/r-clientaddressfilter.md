---
description: 客户端IP地址筛选器。 允许指定一个或多个IP地址或地址范围。
seo-description: 客户端IP地址筛选器。 允许指定一个或多个IP地址或地址范围。
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
uuid: 6a557795-0caf-4b5f-974e-fb4c1481a83c
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 3%

---


# ClientAddressFilter{#clientaddressfilter}

客户端IP地址筛选器。 允许指定一个或多个IP地址或地址范围。

如果指定，则来自未列出IP地址的客户端的此图像目录请求将被拒绝。

## 属性 {#section-d785265988324af68835410c9ba54147}

以逗号分隔的列表IP地址(使用可选网络掩码（CIDR表示法）：

`*`ipAddress`*` `[`/  *`netmask`*`]`*  `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> ddd.ddd.ddd.ddd</span>格式的IP地址。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> netmask</span> </p></td> 
  <td class="stentry"> <p>净蒙版(0...32)。 </p></td> 
 </tr> 
</table>

应用具有`<addressfilter>`元素的预处理规则时，将忽略此属性。

## 默认 {#section-de26e8c9225745e985e4beac1f03f4f6}

如果未定义或为空，则从`default::AddressFilter`继承。

## 示例 {#section-a955314d2b6a4213a16c12a8b18d8627}

无访问限制：`0.0.0.0/0`

授予对所有地址的访问权限（从192开始）：`192.0.0.0/8`

授予对地址介于192.168.12.0和192.168.13.255之间的512台主机的访问权限：`192.168.12.0/23`

授予对单个IP地址的访问权限：`192.168.2.117`或`192.168.2.117/32`

## 另请参阅 {#section-4ea89a7d82e14a4a800487d2d8801465}

[地址筛选器](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
