---
description: 合成模板。 允许指定位于主目录以外的目录中的合成模板。
solution: Experience Manager
title: 模板
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 6%

---

# 模板{#template}

合成模板。 允许您在主目录以外的目录中指定复合模板。

`template= *`模板`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p> </td> 
  <td class="stentry"> <p>模板. </p></td> 
 </tr> 
</table>

*`template`* 必须是包含模板主体的图像目录条目 `catalog::Modifier`.

时间 `template=` 存在，则请求路径中指定的对象不会应用为第0层的源。 但是，它可以作为 `src=` 或 `mask=` 使用预定义的path变量在模板中的任何位置 `$object$` as a `src=` 值。 `catalog::Modifier` 请求路径中指定的对象的ID的值仅适用于 `$object$` 在模板中，而 `catalog::PostModifier` 始终应用。

层0在模板正文中定义，可以是图像、纯色、文本、嵌套或嵌入的请求层。

`catalog:PostModifier` 之 *`object`* 在以下情况下被忽略 *`object`* 用于 `template=`.

## 默认 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

无。

## 属性 {#section-daf3afb1d09c45a6a394468d0874c439}

请求属性。 无论当前图层设置如何，均适用。

## 示例 {#section-9a4f260ed43342b186b0fe855f34bca6}

请参阅中的示例 [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 另请参阅 {#section-067587444f774469931ecafd5a39834c}

[对象](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)， [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)， [预定义的路径变量](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
