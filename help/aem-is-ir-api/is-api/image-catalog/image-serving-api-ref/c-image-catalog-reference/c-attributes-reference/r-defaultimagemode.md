---
description: 默认图像模式。 在找不到请求中指定的图像时，选择如何应用默认图像。
seo-description: 默认图像模式。 在找不到请求中指定的图像时，选择如何应用默认图像。
seo-title: DefaultImageMode
solution: Experience Manager
title: DefaultImageMode
topic: Scene7 Image Serving - Image Rendering API
uuid: e5640f09-e1e3-473b-8fbc-84c6bfce2460
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DefaultImageMode{#defaultimagemode}

默认图像模式。 在找不到请求中指定的图像时，选择如何应用默认图像。

## 属性 {#section-7fa8acb63540490d9f5186231b5e77c3}

枚举。 “0”替换整个合成图像，即使缺失的图像只是几层中的一层；“1”，用默认图像替换每个缺少的图层源图像，并像往常一样返回合成。

## Restrictions {#section-04cb0d50e8914564a8d226d0d4663c8b}

当嵌套的图像渲染、FXG `DefaultImageMode=0` 或请求失败时，图像服务 `req=set` 会恢复为。

## 默认 {#section-9e318524a2a5496386901286748c7ee7}

如果未定义 `default::DefaultImage` 或为空，则从中继承。

## 另请参阅 {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) ，属 [性：:DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
