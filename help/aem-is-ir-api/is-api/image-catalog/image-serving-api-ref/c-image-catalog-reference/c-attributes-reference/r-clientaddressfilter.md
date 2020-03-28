---
description: 客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。
seo-description: 客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a557795-0caf-4b5f-974e-fb4c1481a83c
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# ClientAddressFilter{#clientaddressfilter}

客户端IP地址过滤器。 允许指定一个或多个IP地址或地址范围。

如果指定，则从未列出IP地址的客户端发出的对此图像目录的请求将被拒绝。

## 属性 {#section-d785265988324af68835410c9ba54147}

以逗号分隔的IP地址列表（使用可选网络掩码）:

`*`ipAddress`*``[`/ *`netmask`*`]`*`[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p>ddd.ddd. <span class="varname"> ddd.ddd.ddd格式的IP地址</span> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 网络掩码</span> </p></td> 
  <td class="stentry"> <p>净蒙版(0...32)。 </p></td> 
 </tr> 
</table>

应用含元素的预处理规则时，将忽 `<addressfilter>` 略此属性。

## 默认 {#section-de26e8c9225745e985e4beac1f03f4f6}

如果未定义 `default::AddressFilter` 或为空，则从中继承。

## 示例 {#section-a955314d2b6a4213a16c12a8b18d8627}

无访问限制： `0.0.0.0/0`

授予对所有地址的访问权限（从192开始）: `192.0.0.0/8`

授予对地址介于192.168.12.0和192.168.13.255之间的512台主机的访问权限： `192.168.12.0/23`

授予对单个IP地址的访问权限： `192.168.2.117` or `192.168.2.117/32`

## 另请参阅 {#section-4ea89a7d82e14a4a800487d2d8801465}

[地址过滤器](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
