---
description: ID转换映射。 指定用于将通用图像ID转换为区域设置特定ID的规则。
seo-description: ID转换映射。 指定用于将通用图像ID转换为区域设置特定ID的规则。
seo-title: LocaleMap
solution: Experience Manager
title: LocaleMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 3609a595-2948-43a4-ba8c-fd1a9ea4e26e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# LocaleMap{#localemap}

ID转换映射。 指定用于将通用图像ID转换为区域设置特定ID的规则。

` *`itemitem`*&#42;['|' *``*]`

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

`LocaleMap` 指可映 `locId` 射到任意数量的 `locSuffix`。

Empty *`locSuffix`* values are permitted. *`locSuffix`* 值必须按搜索顺序排序。 返回第一个匹配项。

图像服务会搜 *`locId`* 索与请求中指定的值不区分大小写 `locale=` 的匹配项的值。 如果找到匹配项，则第一个关联 *`locSuffix`* 的值将附加到原始目录ID。 如果此目录条目存在，则使用它，否则将尝 *`locSuffix`* 试下一个值。 如果所有值都 *`locSuffix`* 不与目录条目匹配，图像服务将返回错误或默认图像。

空值匹 *`locId`* 配空字符串和未知 `locale=` 字符串。 这允许为未知区域设置定义默认规则。

启用ID转换后，将应用于引用图像目录和静态内容目录条目的所有ID。

## 属性 {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

一个或多个项目，以|，其中每个项目包含两个或多个以逗号分隔的字符串值。 *`locId`* 并进 `locale=` 行比较。 不区分大小写。

## 另请参阅 {#section-19fba6d5be59439c8bf8ec7513c1a6da}

本地化支 [持，locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)，属 [性：:LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
