---
description: 图像锚点。 此图像用作模板或复合图像中的图层时的原点。
solution: Experience Manager
title: 锚点
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 5%

---

# 锚点{#anchor}

图像锚点。 此图像用作模板或复合图像中的图层时的原点。

还定义旋转的缺省中心点。

## 属性 {#section-95740f14160744e7bc763094b8be40d8}

两个整数数字，以逗号分隔。 相对于全分辨率图像的左上角的像素偏移。

由`anchor=`覆盖（这又可以由`origin=`覆盖）。

## 默认 {#section-ca3a4cc837d643519eff15951f2b47a1}

如果此字段不存在或为空，并且这是有效的图像记录（即，如果`catalog::Path`有效），则使用图像的中心点。

## 另请参阅 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) ,  [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
