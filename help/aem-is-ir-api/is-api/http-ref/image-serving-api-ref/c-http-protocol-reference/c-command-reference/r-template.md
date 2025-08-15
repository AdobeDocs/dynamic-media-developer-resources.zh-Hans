---
title: 模板
description: 合成模板。 允许指定位于主目录以外的目录中的合成模板。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 4%

---

# 模板{#template}

合成模板。 允许您在主目录以外的目录中指定合成模板。

`template= *`模板`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">对象</span> </p> </td> 
  <td class="stentry"> <p>模板。 </p></td> 
 </tr> 
</table>

*`template`*&#x200B;必须是模板正文包含在`catalog::Modifier`中的图像目录条目。

当存在`template=`时，请求路径中指定的对象不会应用为层0的源。 但是，通过使用预定义的路径变量`src=`作为`mask=`值，可以将它作为`$object$`或`src=`引用到模板中的任何位置。 在请求路径中指定的对象的`catalog::Modifier`仅在模板中应用`$object$`的替换，而始终应用`catalog::PostModifier`。

层0在模板主体中定义，可以是图像、纯色、文本、嵌套或嵌入的请求层。

将`catalog:PostModifier`与&#x200B;*`object`*&#x200B;一起使用时，已忽略&#x200B;*`object`*&#x200B;的`template=`。

## 默认 {#section-9de53ea27c4b4fd4811e40e345d8ba05}

无。

## 属性 {#section-daf3afb1d09c45a6a394468d0874c439}

请求属性。 无论当前图层设置如何，均适用。

## 示例 {#section-9a4f260ed43342b186b0fe855f34bca6}

查看[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的示例。

## 另请参阅 {#section-067587444f774469931ecafd5a39834c}

[对象](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)，[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)，[预定义的路径变量](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
