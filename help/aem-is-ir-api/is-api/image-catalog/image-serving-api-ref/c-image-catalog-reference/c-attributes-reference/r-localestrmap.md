---
description: 字符串转换映射。 引用可映射到任意数量的internalLocId的locId。
seo-description: 字符串转换映射。 引用可映射到任意数量的internalLocId的locId。
seo-title: LocaleStrMap
solution: Experience Manager
title: LocaleStrMap
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 44207916-80a6-42cb-8bf1-fcf0f5194c6d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# LocaleStrMap{#localestrmap}

字符串转换映射。 引用可映射到任意数量的internalLocId的locId。

`*`itemitem`*&#42;['|' *``*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 项目 </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> 区域 </span>设 <span class="varname"> 置，  </span>locId*[','  <span class="varname"> locId  </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>区域设置（不区分大小写）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId  </span> </p> </td> 
  <td class="stentry"> <p>内部区域设置ID。 </p> </td> 
 </tr> 
</table>

`LocaleStrMap` 指可以 `locId` 映射到任意数量的 `internalLocId`。

空&#x200B;*`locale`*&#x200B;值与空和未知的`locale=`字符串匹配。 这允许为未知区域设置定义默认规则。

允许空&#x200B;*`locId`*&#x200B;值，并选择&#x200B;*`defaultString`*（*`defaultString`*&#x200B;没有区域设置标识符）。 *`locId`* 按指定的顺序搜索值。返回第一个匹配。

启用字符串转换后，将应用到以下图像目录字段中的文本字符串：

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>目录字段</b> </td> 
   <td> <b>字段中的字符串元素</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::ImageSet  </span> </p> </td> 
   <td> <p>任何包含可翻译字符串的子元素(由分隔符“,”“;”“:”和／或字段的开始/结尾的任意组合分隔)。 </p> <p>可本地化字段开始处的<span class="codeph"> 0xrggbb </span>颜色值从本地化中排除，并且不经修改即通过。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Map  </span> </p> </td> 
   <td> <p>除<span class="codeph"> coords= </span>和<span class="codeph"> shape= </span>属性的值外，任何单引号或多次引号属性值。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 目录：:目标  </span> </p> </td> 
   <td> <p>任何<span class="filepath">目标的值。*.label </span>和<span class="filepath">目标。*.userdata </span>属性。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData  </span> </p> </td> 
   <td> <p>任何属性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-8505a8525f6948ada3979f68c4081044}

一个或多个项目，以 |，其中每个项目包含两个或更多以逗号分隔的字符串值。

## 另请参阅 {#section-0c0516e4f83d42d38247308cab9b6708}

本地化支持，[locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb),[属性：:LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318),[目录：:ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md),[目录：:Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md),[目录：目标](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md),[目录：userData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
