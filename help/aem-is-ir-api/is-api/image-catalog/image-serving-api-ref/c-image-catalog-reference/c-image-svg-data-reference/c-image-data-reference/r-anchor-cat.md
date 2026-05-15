---
description: 图像锚点。 此图像用作模板或复合图像中的图层时的原点。
solution: Experience Manager
title: 锚点
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
TQID: 'https://experienceleague.adobe.com/OKTbXTF3uzVcQeLQIGIJhCukQFzdW5gZMzatSdWP7yY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 4%

---

# 锚点{#anchor}

图像锚点。 此图像用作模板或复合图像中的图层时的原点。

还定义旋转的默认中心点。

## 属性 {#section-95740f14160744e7bc763094b8be40d8}

用逗号分隔的两个整数。 相对于全分辨率图像左上角的像素偏移。

已由`anchor=`覆盖（这又可以由`origin=`覆盖）。

## 默认 {#section-ca3a4cc837d643519eff15951f2b47a1}

如果此字段不存在或为空，并且这是有效的图像记录（即，`catalog::Path`是否有效），则使用图像的中心点。

## 另请参阅 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) ， [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
