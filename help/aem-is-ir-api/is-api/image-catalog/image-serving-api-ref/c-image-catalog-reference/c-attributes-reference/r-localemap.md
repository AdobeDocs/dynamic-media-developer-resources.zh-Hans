---
description: ID转换映射。 指定用于将通用图像ID转换为特定于区域设置的ID的规则。
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---

# LocaleMap{#localemap}

ID转换映射。 指定用于将通用图像ID转换为特定于区域设置的ID的规则。

`*`项目`*&#42;['|' *`项目`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 项目</span> </p></td> 
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

`LocaleMap` 是指 `locId` 可以映射到任意数量的受众 `locSuffix`.

空 *`locSuffix`* 值是允许的。 *`locSuffix`* 值必须按搜索顺序排序。 返回第一个匹配项。

图像服务搜索 *`locId`* 不区分大小写的值与 `locale=` 请求中指定的值。 如果找到匹配项，则第一个关联的 *`locSuffix`* 值将附加到原始目录id。 如果此目录条目存在，则使用它，否则使用下一个 *`locSuffix`* 值已尝试。 如果所有 *`locSuffix`* 值与目录条目匹配，图像服务返回错误或默认图像。

空 *`locId`* 值匹配空和未知 `locale=` 字符串。 这允许为未知区域设置定义默认规则。

ID翻译在启用时应用到引用图像目录和静态内容目录条目的所有ID。

## 属性 {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

一个或多个项目，用分隔 |，其中每个项目由两个或更多逗号分隔的字符串值组成。 *`locId`* 和 `locale=` 比较。 不区分大小写。

## 另请参阅 {#section-19fba6d5be59439c8bf8ec7513c1a6da}

本地化支持， [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)， [attribute：：LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
