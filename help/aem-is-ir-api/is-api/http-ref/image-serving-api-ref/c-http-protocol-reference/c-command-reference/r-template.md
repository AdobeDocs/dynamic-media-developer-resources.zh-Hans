---
description: 合成模板。 允许指定位于除主目录以外的目录中的合成模板。
solution: Experience Manager
title: 模板
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 6%

---

# 模板{#template}

合成模板。 用于在除主目录以外的目录中指定合成模板。

`template= *`模板`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p> </td> 
  <td class="stentry"> <p>模板. </p></td> 
 </tr> 
</table>

*`template`* 必须是包含模板正文的图像目录条目 `catalog::Modifier`。

当存在`template=`时，请求路径中指定的对象将不应用为层0的源。 但是，可以使用预定义路径变量`$object$`作为`src=`值，将其作为模板中的任意位置引用为`src=`或`mask=`。 `catalog::Modifier` 在请求路径中指定的对象的，仅在模板内 `$object$` 应用替换，而 `catalog::PostModifier` 始终应用。

层0在模板主体中定义，可以是图像、纯色、文本、嵌套或嵌入的请求层。

`catalog:PostModifier` 与一起 *`object`* 使用时， *`object`* 将忽略 `template=`。

## 默认 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

无。

## 属性 {#section-daf3afb1d09c45a6a394468d0874c439}

请求属性。 无论当前的层设置如何，都适用。

## 示例 {#section-9a4f260ed43342b186b0fe855f34bca6}

请参阅[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的示例。

## 另请参阅 {#section-067587444f774469931ecafd5a39834c}

[对象](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)、模 [板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)、预定义 [路径变量](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
