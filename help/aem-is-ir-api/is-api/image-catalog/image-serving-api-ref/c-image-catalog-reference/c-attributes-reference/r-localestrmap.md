---
description: 字符串翻译映射。 是指可以映射到任意数量的internalLocId的locId。
solution: Experience Manager
title: 区域设置字符串映射
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

---

# 区域设置字符串映射{#localestrmap}

字符串翻译映射。 是指可以映射到任意数量的internalLocId的locId。

`*`项目`*&#42;['|' *`项目`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 项目 </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> 区域设置 </span>， <span class="varname"> locId </span>*['，' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>区域设置（区分大小写）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>内部区域设置ID </p> </td> 
 </tr> 
</table>

`LocaleStrMap` 是指 `locId` 可以映射到任意数量的受众 `internalLocId`.

空 *`locale`* 值匹配空和未知 `locale=` 字符串。 这允许为未知区域设置定义默认规则。

空 *`locId`* 值是允许的，请选择 *`defaultString`* (此 *`defaultString`* 没有区域设置标识符)。 *`locId`* 按指定的顺序搜索值。 返回第一个匹配项。

字符串翻译在启用时应用到以下图像目录字段中的文本字符串：

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>目录字段</b> </td> 
   <td> <b>字段中的字符串元素</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog：：图像集 </span> </p> </td> 
   <td> <p>包含可翻译字符串的任何子元素（由分隔符“，”“；”“：”和/或字段的开头/结尾的任何组合分隔）。 </p> <p>A <span class="codeph"> 0xrrggbb </span> 可本地化字段开头的颜色值将从本地化中排除，并且无需修改即可传递。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog：：Map </span> </p> </td> 
   <td> <p>任何单引号或双引号属性值，但 <span class="codeph"> 坐标= </span> 和 <span class="codeph"> shape= </span> 属性。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog：：目标 </span> </p> </td> 
   <td> <p>任何值 <span class="filepath"> 目标。*.label </span> 和 <span class="filepath"> 目标。*.userdata </span> 属性。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog：：UserData </span> </p> </td> 
   <td> <p>任何属性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-8505a8525f6948ada3979f68c4081044}

一个或多个项目，用分隔 |，其中每个项目由两个或更多以逗号分隔的字符串值组成。

## 另请参阅 {#section-0c0516e4f83d42d38247308cab9b6708}

本地化支持， [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)， [attribute：：LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318)， [catalog：：图像集](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)， [catalog：：Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md)， [catalog：：目标](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)， [catalog：：UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
