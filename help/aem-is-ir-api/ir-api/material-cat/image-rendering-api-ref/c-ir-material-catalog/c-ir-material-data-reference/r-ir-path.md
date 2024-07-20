---
description: 图像文件路径。 纹理或贴花图像文件的相对路径和名称。
solution: Experience Manager
title: 路径*
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---

# 路径*{#path}

图像文件路径。 纹理或贴花图像文件的相对路径和名称。

服务器将此值与`attribute::RootPath`合并以生成实际的图像文件路径。 也可以是绝对路径。

用于指定纹理、橱柜和窗口覆盖材料的纹理图像文件，以及贴花和墙壁边界材料的RGB或RGBA图像文件。 并非所有的机柜和窗户覆盖材料都需要单独的可重复纹理图像。

## 属性 {#section-8c12ea24f21d4472be677581893e6681}

文本字符串。 纹理和贴花材料所需，机柜和窗户覆盖材料可选。 如果指定，则必须是有效的相对或绝对文件路径。 纯色材料必须为空。

## 支持的文件格式 {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

图像渲染支持与Dynamic Media图像服务相同的源图像格式。

当使用Dynamic Media金字塔TIFF(PTIFF)多分辨率格式时，需要多个不同分辨率的图像数据的应用程序性能最佳。 图像服务包括从任何支持的格式创建PTIFF图像的图像转换器(IC)实用程序。

有关支持的文件格式的完整列表，请参阅图像服务文档中的IC实用程序描述。

## 默认 {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

无。

## 另请参阅 {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[IC实用程序](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ，[属性：：RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md)，[src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
