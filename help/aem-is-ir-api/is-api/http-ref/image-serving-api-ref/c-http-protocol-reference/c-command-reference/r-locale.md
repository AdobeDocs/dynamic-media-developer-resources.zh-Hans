---
description: 翻译区域设置ID。 指定请求的区域设置ID。
seo-description: 翻译区域设置ID。 指定请求的区域设置ID。
seo-title: 区域设置
solution: Experience Manager
title: 区域设置
uuid: 82acc0bb-fd94-44c9-8ff9-3b9cefab4627
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 5%

---


# locale{#locale}

翻译区域设置ID。 指定请求的区域设置ID。

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>区域设置ID（字符串）。 </p></td> 
 </tr> 
</table>

使用此id和使用`attribute::LocaleMap`和`attribute::LocaleStrMap`指定的规则，图像服务应用可选的目录id转换和字符串本地化。

## 属性 {#section-1854a9902b884d9b8e8e713b6635723f}

请求命令。 应用于整个请求，包括嵌套/嵌入的请求，而不管它在何处指定。 `locId` 必须只包含可打印的ASCII字符。如果此请求的主目录中未定义本地化映射，则忽略。 如果指定了空或无效的`locId`，并且未在`attribute::DefaultLocale`中定义默认规则，则返回错误。

## 默认 {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` 当未指定locale=时使用。

## 另请参阅 {#section-28a586d43ac4429d98e318a580c92af4}

[attribute:::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) , [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318),attribute [::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e),本地化支持
