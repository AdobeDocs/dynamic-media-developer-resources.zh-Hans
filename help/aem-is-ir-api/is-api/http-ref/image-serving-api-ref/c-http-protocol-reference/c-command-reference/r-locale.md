---
title: 区域设置
description: 翻译区域设置ID。 指定请求的区域设置ID。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d937dfa5-95dd-49fd-ac23-e77e07b0642c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# 区域设置{#locale}

翻译区域设置ID。 指定请求的区域设置ID。

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>区域设置ID（字符串）。 </p></td> 
 </tr> 
</table>

使用此ID和指定的规则 `attribute::LocaleMap` 和 `attribute::LocaleStrMap`，图像服务应用可选的目录ID翻译和字符串本地化。

## 属性 {#section-1854a9902b884d9b8e8e713b6635723f}

请求命令。 适用于整个请求，包括嵌套/嵌入请求，无论在何处指定。 `locId` 只能包含可打印的ASCII字符。 如果未在此请求的主目录中定义本地化映射，则忽略。 如果为空或无效，则返回错误 `locId` 已指定，并且未在中定义默认规则 `attribute::DefaultLocale`.

## 默认 {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` 当未指定locale=时使用。

## 另请参阅 {#section-28a586d43ac4429d98e318a580c92af4}

[attribute：：DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) ， [attribute：：LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318)， [attribute：：LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)，本地化支持
