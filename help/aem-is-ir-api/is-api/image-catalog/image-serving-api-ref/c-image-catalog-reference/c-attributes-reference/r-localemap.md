---
description: ID转换映射。 指定用于将通用图像ID转换为特定于区域设置的ID的规则。
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# LocaleMap{#localemap}

ID转换映射。 指定用于将通用图像ID转换为特定于区域设置的ID的规则。

`*`项`*&#42;['|' *`项`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">项</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>，<span class="varname"> locSuffix</span>*['，'<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>区域设置ID（不区分大小写）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>区域设置后缀。 </p></td> 
 </tr> 
</table>

`LocaleMap`引用的`locId`可以映射到任意数量的`locSuffix`。

允许空的&#x200B;*`locSuffix`*&#x200B;值。 *`locSuffix`*&#x200B;值必须按搜索顺序排序。 返回第一个匹配项。

图像服务在&#x200B;*`locId`*&#x200B;值中搜索与请求中指定的`locale=`值不区分大小写的匹配。 如果找到匹配项，则第一个关联的&#x200B;*`locSuffix`*&#x200B;值将附加到原始目录ID。 如果此目录条目存在，则使用该条目，否则尝试下一个&#x200B;*`locSuffix`*&#x200B;值。 如果&#x200B;*`locSuffix`*&#x200B;值都不与目录条目匹配，则图像服务返回错误或默认图像。

空&#x200B;*`locId`*&#x200B;值与空和未知`locale=`字符串匹配。 这允许为未知区域设置定义默认规则。

ID转换在启用时应用到引用图像目录和静态内容目录条目的所有ID。

## 属性 {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

一个或多个项目，用分隔 |，其中每一项由两个或更多逗号分隔的字符串值组成。 *`locId`*&#x200B;和`locale=`已比较。 不区分大小写。

## 另请参阅 {#section-19fba6d5be59439c8bf8ec7513c1a6da}

本地化支持，[区域设置=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)，[属性：：LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
