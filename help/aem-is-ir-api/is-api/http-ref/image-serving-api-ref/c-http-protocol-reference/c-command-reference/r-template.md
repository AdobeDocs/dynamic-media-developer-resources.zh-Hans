---
description: 合成模板。 允许指定位于除主目录之外的目录中的合成模板。
seo-description: 合成模板。 允许指定位于除主目录之外的目录中的合成模板。
seo-title: 模板
solution: Experience Manager
title: 模板
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b37d60-1d0c-4d0b-a5a0-98d8bf9e9064
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 模板{#template}

合成模板。 允许指定位于除主目录之外的目录中的合成模板。

`template= *`模板`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p> </td> 
  <td class="stentry"> <p>模板. </p></td> 
 </tr> 
</table>

*`template`* 必须是包含模板正文的图像目录条目 `catalog::Modifier`。

当存 `template=` 在时，在请求路径中指定的对象将不会作为层0的源应用，但可以作为模板中的一个或任意位置引用，方法是使用预定义的路径变量 `src=` 作为 `mask=``$object$``src=` 值。 `catalog::Modifier` 在请求路径中指定的对象的替换仅与模板中的替换有关 `$object$` 而应用，而始 `catalog::PostModifier` 终应用。

层0在模板主体中定义，可以是图像、纯色、文本或嵌套或嵌入的请求层。

`catalog:PostModifier` 与一 *`object`* 起使用时 *`object`* 将忽略 `template=`。

## 默认 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

无。

## 属性 {#section-daf3afb1d09c45a6a394468d0874c439}

请求属性。 无论当前图层设置如何，均可应用。

## 示例 {#section-9a4f260ed43342b186b0fe855f34bca6}

请参阅模板中的 [示例](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另请参阅 {#section-067587444f774469931ecafd5a39834c}

[对象](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)，模 [板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)，预定义 [的路径变量](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
