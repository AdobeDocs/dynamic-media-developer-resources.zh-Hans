---
title: 根路径
description: Source数据根路径。 文本字符串值。 此图像目录引用的所有晕影、纹理、图像和ICC数据文件的根文件夹的绝对路径或相对路径区段。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# 根路径{#rootpath}

Source数据根路径。 文本字符串值。 此图像目录引用的所有晕影、纹理、图像和ICC数据文件的根文件夹的绝对路径或相对路径区段。

## 属性 {#section-5ff1cf592dd24dfc8cfa470c753ab828}

文本字符串。 必须为空、相对于图像渲染服务器配置设置`ir.resourceRootPaths`的有效路径区段或有效的绝对文件路径。 不应包含前导和尾随路径元素分隔符。

## 默认 {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

如果未定义，则从`default::RootPath`继承。 如果已定义但为空，则它不会参与源文件根路径。

## 另请参阅 {#section-92012cc1ce32448ea977e7e0484857e2}

[目录：：Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) ，[目录：：AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969)，`ir.resourceRootPaths`
