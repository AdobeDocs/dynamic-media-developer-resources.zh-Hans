---
description: 图像蒙版。 指定单独的蒙版图像以用作未关联的蒙版。
solution: Experience Manager
title: 蒙版
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 1%

---

# 蒙版{#mask}

图像蒙版。 指定单独的蒙版图像以用作未关联的蒙版。

`mask= *``*|{[is|ir]'{' *`objectnestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p></td> 
  <td class="stentry"> <p>用作图像或图层蒙版的图像对象。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>嵌套图像提供、图像呈现或外部请求。 </p></td> 
 </tr> 
</table>

*`object`* 可以是目录条目或图像/SVG文件。可以为图像层和纯色层指定。

如果&#x200B;*`object`*&#x200B;解析为图像目录条目，则使用`catalog::MaskPath`；或者，如果未定义`catalog::MaskPath`，则使用`catalog::Path`。 如果&#x200B;*`object`*&#x200B;未解析为目录条目，则会将其解释为文件路径。

在所有情况下，如果源图像具有Alpha通道，则会使用该通道。 否则，在将图像用作图层蒙版之前，如有必要，会将其转换为灰度。

如果蒙版附加到实色图层，则可以使用与图像图层中图像相同的规则裁剪和缩放蒙版。 `size=`、  `scale=`或 `res=` 可用于缩放蒙版。

也可以以&#x200B;*`nestedRequest`*&#x200B;的形式指定图层蒙版。 嵌套或嵌入的请求以大括号括起来。 为嵌入式图像提供请求添加`is`前缀，为嵌入式图像呈现请求添加`ir`前缀。 如果未指定前缀，则假定对外来服务器的请求。 有关详细信息，请参阅[请求嵌套和嵌入](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)。

## 属性 {#section-a093043dc249423b8ae322cefb0d545d}

图像或图层属性。 如果`layer=comp`，则应用于层0。 被效果层忽略。

*`object`* 不能解析为目录记录，该目录记录在中 `src=` 包含 `mask=` 或 `catalog::Modifier`命令。

`is`和`ir`前缀不区分大小写。

## 默认 {#section-10cf793c665f49deb1b248faa3b618a9}

如果未明确指定`mask=`，并且层图像与目录条目相关联，则使用`catalog::MaskPath`。 否则，如果存在，则使用层图像的Alpha通道。 如果没有Alpha通道，则该层没有蒙版，并且该层矩形呈现为完全不透明。

## 示例 {#section-1bbe623f7c744bdf97b596458d8e7ea3}

使用多个单独的蒙版来着色图像的不同区域。 已着色的蒙版区域在原始未修改图像的上方分层：

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## 另请参阅 {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) ,  [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),  [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) ,  [Request Nesting and Embedding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
