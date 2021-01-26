---
description: 数据文件路径。 与此图像关联的非图像数据文件的相对路径和名称。
seo-description: 数据文件路径。 与此图像关联的非图像数据文件的相对路径和名称。
seo-title: AuxPath
solution: Experience Manager
title: AuxPath
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 95d28f8d-27ec-480a-a62a-7e5e8fbfb3fb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 3%

---


# AuxPath{#auxpath}

数据文件路径。 与此图像关联的非图像数据文件的相对路径和名称。

服务器将此值与属性：:RootPath结合，以构建实际的文件路径。 也可以是绝对文件路径。

用于指定机柜材料的机柜样式文件或窗口覆盖材料的窗口覆盖样式文件。 留空以处理所有其他材料。

## 属性 {#section-4268350054b7421da0ce0327f0731a52}

文本字符串值。 如果指定，则它必须是有效的相对或绝对文件路径。 橱柜材料和窗盖材料要求。 对于所有其他材料必须为空。

## 默认 {#section-287005c2d8e948fa958f69ba7b90b437}

无。

## 另请参阅 {#section-e1f7a61c00d04a80af28e2e67481ab92}

[属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) , [目录：:Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590), [ src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
