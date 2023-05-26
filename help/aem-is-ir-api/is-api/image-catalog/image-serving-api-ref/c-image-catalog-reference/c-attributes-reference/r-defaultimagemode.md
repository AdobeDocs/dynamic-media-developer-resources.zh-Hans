---
description: 默认图像模式。 选择当在请求中指定的图像未找到时如何应用默认图像。
solution: Experience Manager
title: 默认图像模式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b30ce72f-7c74-407c-bd4a-042b84c469e9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---

# 默认图像模式{#defaultimagemode}

默认图像模式。 选择当在请求中指定的图像未找到时如何应用默认图像。

## 属性 {#section-7fa8acb63540490d9f5186231b5e77c3}

枚举。 “0”表示替换整个复合图像，即使缺少的图像只是多个图层之一也是如此；“1”表示使用默认图像替换每个缺少的图层源图像并照常返回复合图像。

## 限制 {#section-04cb0d50e8914564a8d226d0d4663c8b}

图像服务恢复为 `DefaultImageMode=0` 嵌套图像渲染、FXG或 `req=set` 请求失败。

## 默认 {#section-9e318524a2a5496386901286748c7ee7}

继承自 `default::DefaultImage` 如果未定义或为空。

## 另请参阅 {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[默认图像=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) ， [attribute：：DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
