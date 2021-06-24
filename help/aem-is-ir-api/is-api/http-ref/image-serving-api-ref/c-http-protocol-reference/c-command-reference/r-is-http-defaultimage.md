---
description: 默认回复图像。 指定在找不到图像时要使用的图像或目录条目。
solution: Experience Manager
title: defaultImage
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 741833b5-e858-4aa5-96c1-bb06539deef3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# defaultImage{#defaultimage}

默认回复图像。 指定在找不到图像时要使用的图像或目录条目。

` defaultImage= *`object`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 对象  </span> </span> </p> </td> 
  <td class="stentry"> <p>图像对象。 </p> </td> 
 </tr> 
</table>

*`object`* 可以是目录条目（包括模板）或简单的图像文件路径。用默认图像替换缺少的图像非常有用。 此值覆盖相应目录`attribute::DefaultImage`的值。 空值(`defaultImage=`)会禁用默认图像处理。

>[!NOTE]
>
>默认图像机制不适用于SVG对象。 如果找不到请求中指定的SVG对象，则返回错误。

如果`attribute::DefaultImageMode=0`，则&#x200B;*`object`*&#x200B;会替换整个原始请求，即使多图像组合中只缺少一个图像也是如此。 从原始请求中保留的唯一命令是：`wid=`、`hei=`、`fmt=`、`qlt=`。

如果`attribute::DefaultImageMode=1`，则对象仅替换缺失的图层图像；将应用缺少层的属性，并照常处理和返回复合。

## 属性 {#section-d30923d8dc4042eba10989212dd70887}

请求属性。 无论当前的层设置如何，都适用。 如果`req=`不是`img`或`tmb`，则忽略。

## 限制 {#section-30df31bc8cac41cd917f1e45196779c2}

默认图像机制不覆盖外来图像源；如果外来图像源无效，则返回错误。

当嵌套的“图像渲染”或FXG渲染请求失败时，“图像服务”会还原为`DefaultImageMode=0`。

## 默认 {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## 另请参阅 {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [attribute:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [ *`object`* ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
