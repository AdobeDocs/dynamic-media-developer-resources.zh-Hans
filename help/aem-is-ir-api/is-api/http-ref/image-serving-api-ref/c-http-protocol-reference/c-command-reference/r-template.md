---
description: 合成模板。 允许指定位于除主目录之外的目录中的合成模板。
solution: Experience Manager
title: 模板
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 6%

---


# 模板{#template}

合成模板。 允许您在除主目录之外的目录中指定合成模板。

`template= *`模板`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p> </td> 
  <td class="stentry"> <p>模板. </p></td> 
 </tr> 
</table>

*`template`* 必须是包含模板正文的图像目录条目 `catalog::Modifier`。

当存在`template=`时，在请求路径中指定的对象不会作为层0的源应用。 但是，可以使用预定义的路径变量`$object$`作为`src=`值，将其作为模板中的任何位置的`src=`或`mask=`进行引用。 `catalog::Modifier` 在请求路径中指定的对象的替代仅在模板中 `$object$` 应用，而始终 `catalog::PostModifier` 应用。

图层0在模板主体中定义，可以是图像、纯色、文本或嵌套或嵌入的请求图层。

`catalog:PostModifier` 与 *`object`* 一起使用时 *`object`* 将忽略 `template=`of。

## 默认 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

无。

## 属性 {#section-daf3afb1d09c45a6a394468d0874c439}

请求属性。 无论当前图层设置如何，均适用。

## 示例 {#section-9a4f260ed43342b186b0fe855f34bca6}

请参见[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的示例。

## 另请参阅 {#section-067587444f774469931ecafd5a39834c}

[对象](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)、模 [板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)、预 [定义路径变量](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
