---
description: ID转换映射。 指定用于将通用图像ID转换为特定于区域设置的ID的规则。
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 1%

---

# LocaleMap{#localemap}

ID转换映射。 指定用于将通用图像ID转换为特定于区域设置的ID的规则。

`*``*&#42;['|' *`itemitem`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 项目</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
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

`LocaleMap` 是指可 `locId` 映射到任意数量的 `locSuffix`。

允许使用空&#x200B;*`locSuffix`*&#x200B;值。 *`locSuffix`* 值必须按照其搜索顺序进行排序。返回第一个匹配项。

图像服务会搜索&#x200B;*`locId`*&#x200B;值，以查找与请求中指定的`locale=`值不区分大小写的匹配项。 如果找到匹配项，则关联的第一个&#x200B;*`locSuffix`*&#x200B;值会附加到原始目录ID中。 如果存在此目录条目，则使用它，否则将尝试下一个&#x200B;*`locSuffix`*&#x200B;值。 如果&#x200B;*`locSuffix`*&#x200B;值中没有一个与目录条目匹配，则图像服务会返回错误或默认图像。

空&#x200B;*`locId`*&#x200B;值与空和未知的`locale=`字符串匹配。 这允许为未知区域设置定义默认规则。

ID转换在启用后会应用于引用图像目录和静态内容目录条目的所有ID。

## 属性 {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

一个或多个项目，以 |，其中每个项目包含两个或更多以逗号分隔的字符串值。 *`locId`* 和进 `locale=` 行比较。不区分大小写。

## 另请参阅 {#section-19fba6d5be59439c8bf8ec7513c1a6da}

本地化支持， [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
