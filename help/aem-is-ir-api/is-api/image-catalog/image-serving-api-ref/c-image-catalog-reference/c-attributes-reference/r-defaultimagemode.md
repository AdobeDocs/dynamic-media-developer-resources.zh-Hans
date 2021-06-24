---
description: 默认图像模式。 选择在找不到请求中指定的图像时应用默认图像的方式。
solution: Experience Manager
title: DefaultImageMode
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: b30ce72f-7c74-407c-bd4a-042b84c469e9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# DefaultImageMode{#defaultimagemode}

默认图像模式。 选择在找不到请求中指定的图像时应用默认图像的方式。

## 属性 {#section-7fa8acb63540490d9f5186231b5e77c3}

枚举。 “0”替换整个复合图像，即使缺少的图像只是几层中的一层；“1”将每个缺失的层源图像替换为默认图像，并照常返回复合图像。

## 限制 {#section-04cb0d50e8914564a8d226d0d4663c8b}

当嵌套的图像渲染、FXG或`req=set`请求失败时，图像服务会还原为`DefaultImageMode=0`。

## 默认 {#section-9e318524a2a5496386901286748c7ee7}

从`default::DefaultImage`继承（如果未定义或为空）。

## 另请参阅 {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) ,  [attribute::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
