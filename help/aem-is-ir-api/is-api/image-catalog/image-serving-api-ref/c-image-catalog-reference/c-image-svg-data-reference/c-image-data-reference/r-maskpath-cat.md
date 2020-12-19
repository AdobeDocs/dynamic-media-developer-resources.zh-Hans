---
description: 遮罩文件路径。 与此目录记录关联的蒙版图像文件的相对或绝对路径和名称。
seo-description: 遮罩文件路径。 与此目录记录关联的蒙版图像文件的相对或绝对路径和名称。
seo-title: 蒙版路径
solution: Experience Manager
title: 蒙版路径
topic: Scene7 Image Serving - Image Rendering API
uuid: a2d1f08a-0a26-41a6-9be2-f5cc2afb15c4
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---


# MaskPath{#maskpath}

遮罩文件路径。 与此目录记录关联的蒙版图像文件的相对或绝对路径和名称。

允许将单独的蒙版附加到图像。

服务器使用[管理源数据](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md)中所述的路径解析规则来查找数据文件。

## 属性 {#section-cdc3b7e2811e41008479cd97887c01b7}

文本字符串值。 可选。如果指定，则它必须是有效的相对或绝对图像服务器文件路径。 `attribute::DefaultExt` 如果不存在文件后缀，则附加。

如果在目录记录中同时定义主图像(`catalog::Path`)和遮罩图像(`catalog::MaskPath`)，则二者的像素大小必须完全相同。 蒙版图像必须为8位灰度。

`mask=` 的双曲余切值 `catalog::MaskPath`。

`catalog::MaskPath` 重写主图像()中的 `catalog::Path`alpha渠道（如果存在），如果alpha渠道未关联（即未预乘）。如果图像alpha已预乘，则忽略`catalog::MaskPath`，并始终使用alpha渠道。

## 默认 {#section-78533e35bfec469ba087cb68a35bb81b}

无。

## 另请参阅 {#section-68d262f5949c4959b8723ba44611d1dc}

[属性：:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [属性：:DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [目录：:Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c),  [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md),  [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
