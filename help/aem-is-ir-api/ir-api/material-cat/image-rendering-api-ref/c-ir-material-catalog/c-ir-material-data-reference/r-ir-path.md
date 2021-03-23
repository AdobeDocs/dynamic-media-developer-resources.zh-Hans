---
description: 图像文件路径。 纹理或贴图像文件的相对路径和名称。
seo-description: 图像文件路径。 纹理或贴图像文件的相对路径和名称。
seo-title: 路径 *
solution: Experience Manager
title: 路径 *
uuid: 9e85a358-3f2f-4b8b-a98f-03de2a1a8a4c
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---


# 路径 *{#path}

图像文件路径。 纹理或贴图像文件的相对路径和名称。

服务器将此值与`attribute::RootPath`组合，以生成实际的图像文件路径。 也可以是绝对路径。

用于为纹理、机柜和窗口覆盖材料指定纹理图像文件，为贴面和壁边框材料指定RGB或RGBA图像文件。 并非所有的机柜和窗口覆盖材料都需要单独的可重复纹理图像。

## 属性 {#section-8c12ea24f21d4472be677581893e6681}

文本字符串。 纹理和贴面材料要求，机柜和窗口覆盖材料可选。 如果指定，则它必须是有效的相对或绝对文件路径。 对于纯色材料，必须为空。

## 支持的文件格式{#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

图像渲染支持与Dynamic Media图像服务相同的源图像格式。

使用Dynamic Media金字塔TIFF(PTIFF)多分辨率格式时，需要多个不同分辨率的图像数据的应用程序性能最好。 图像服务包括图像转换器(IC)实用程序，它可从任何支持的格式创建PTIFF图像。

有关所支持文件格式的完整列表，请参阅图像服务文档中IC实用程序的说明。

## 默认 {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

无。

## 另请参阅 {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[IC实用程](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) 序， [属性：:Root](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md)Path [, src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
