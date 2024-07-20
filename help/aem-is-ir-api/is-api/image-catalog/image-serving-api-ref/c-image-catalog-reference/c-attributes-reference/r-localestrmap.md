---
description: 字符串翻译映射。 引用可以映射到任意数量的internalLocId的locId。
solution: Experience Manager
title: 区域设置字符串映射
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# 区域设置字符串映射{#localestrmap}

字符串翻译映射。 引用可以映射到任意数量的internalLocId的locId。

`*`项`*&#42;['|' *`项`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">项</span> </p> </td> 
  <td class="stentry"> <p> <span class="varname">区域设置</span>，<span class="varname"> locId </span>*['，' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">区域设置</span> </p> </td> 
  <td class="stentry"> <p>区域设置（不区分大小写）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>内部区域设置ID。 </p> </td> 
 </tr> 
</table>

`LocaleStrMap`引用的`locId`可以映射到任意数量的`internalLocId`。

空&#x200B;*`locale`*&#x200B;值与空和未知`locale=`字符串匹配。 这允许为未知区域设置定义默认规则。

允许空&#x200B;*`locId`*&#x200B;值并选择&#x200B;*`defaultString`*（*`defaultString`*&#x200B;没有区域设置标识符）。 *`locId`*&#x200B;值按指定的顺序搜索。 返回第一个匹配项。

字符串翻译在启用时应用到以下图像目录字段中的文本字符串：

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>目录字段</b> </td> 
   <td> <b>字符串元素在字段</b>中 </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">目录：：图像集</span> </p> </td> 
   <td> <p>包含可翻译字符串的任何子元素（由分隔符“，”“；”“：”和/或字段的开始/结束位置的任何组合分隔）。 </p> <p>可本地化字段开头的<span class="codeph"> 0xrrggbb </span>颜色值从本地化中排除，无需修改即可传递。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">目录：：映射</span> </p> </td> 
   <td> <p>任何单引号或双引号属性值，但<span class="codeph">坐标= </span>和<span class="codeph">形状= </span>属性的值除外。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">目录：：目标</span> </p> </td> 
   <td> <p>任何<span class="filepath">目标的值。*.label </span>和<span class="filepath">目标*.userdata </span>属性。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">目录：：UserData </span> </p> </td> 
   <td> <p>任何属性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-8505a8525f6948ada3979f68c4081044}

一个或多个项目，用分隔 |，其中每一项由两个或更多以逗号分隔的字符串值组成。

## 另请参阅 {#section-0c0516e4f83d42d38247308cab9b6708}

本地化支持，[区域设置=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)，[属性：：LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318)，[目录：：图像集](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)，[目录：：Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md)，[目录：：Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)，[目录：：UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
