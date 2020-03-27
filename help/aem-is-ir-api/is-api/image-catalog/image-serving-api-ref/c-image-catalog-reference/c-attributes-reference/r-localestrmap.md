---
description: 字符串转换映射。 引用可映射到任意数量internalLocId的locId。
seo-description: 字符串转换映射。 引用可映射到任意数量internalLocId的locId。
seo-title: LocaleStrMap
solution: Experience Manager
title: LocaleStrMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 44207916-80a6-42cb-8bf1-fcf0f5194c6d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# LocaleStrMap{#localestrmap}

字符串转换映射。 引用可映射到任意数量internalLocId的locId。

` *`itemitem`*&#42;['|' *``*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 项目 </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale </span>, <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>区域设置（不区分大小写）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>内部区域设置ID。 </p> </td> 
 </tr> 
</table>

`LocaleStrMap` 指可映 `locId` 射到任意数量的 `internalLocId`。

空值匹 *`locale`* 配空字符串和未知 `locale=` 字符串。 这允许为未知区域设置定义默认规则。

允许 *`locId`* 使用空值，并选择 *`defaultString`* (区 *`defaultString`* 域设置标识符没有)。 *`locId`* 按指定的顺序搜索值。 返回第一个匹配项。

启用字符串转换后，将应用于以下图像目录字段中的文本字符串：

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>目录字段</b> </td> 
   <td> <b>字段中的字符串元素</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>包含可翻译字符串的任何子元素(由分隔符',' ';' ':'和／或字段的开始/结尾的任意组合分隔)。 </p> <p>可本 <span class="codeph"> 地化字 </span> 段开头的0xrrggbb颜色值从本地化中排除并传递而不进行修改。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Map </span> </p> </td> 
   <td> <p>除coords=和shape=属性的值外，任何单引号或多次引号的 <span class="codeph"> 属性值 </span> 都 <span class="codeph"> 是 </span> 例外。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目录：:目标 </span> </p> </td> 
   <td> <p>任何目标的 <span class="filepath"> 值。*.label </span> 和 <span class="filepath"> 目标。*.userdata属 </span> 性。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>任何属性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-8505a8525f6948ada3979f68c4081044}

一个或多个项目，以|，其中每个项目包含两个或多个以逗号分隔的字符串值。

## 另请参阅 {#section-0c0516e4f83d42d38247308cab9b6708}

本地化支 [持：locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)，属性：:MapMap [,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318)目录：SetImageSet [，目](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)[](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md)[](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)[录：目录：目录目标，目录：目录：：目录，用户数据](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
