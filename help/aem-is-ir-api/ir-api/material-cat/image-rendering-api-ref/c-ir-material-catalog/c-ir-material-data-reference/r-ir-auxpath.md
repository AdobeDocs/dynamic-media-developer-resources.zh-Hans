---
description: 数据文件路径。 与此图像关联的非图像数据文件的相对路径和名称。
solution: Experience Manager
title: AuxPath
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 55f82596-72f0-48c4-9b3a-f10ea5f610f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# AuxPath{#auxpath}

数据文件路径。 与此图像关联的非图像数据文件的相对路径和名称。

服务器将此值与属性：:RootPath组合在一起，以构建实际的文件路径。 也可以是绝对文件路径。

用于为机柜材料指定机柜样式文件或为窗口覆盖材料指定窗口覆盖样式文件。 留空以备所有其他材料。

## 属性 {#section-4268350054b7421da0ce0327f0731a52}

文本字符串值。 如果指定，则必须是有效的相对或绝对文件路径。 需要使用机柜材料和窗盖材料。 对于所有其他材料，必须为空。

## 默认 {#section-287005c2d8e948fa958f69ba7b90b437}

无。

## 另请参阅 {#section-e1f7a61c00d04a80af28e2e67481ab92}

[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) ,  [catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
