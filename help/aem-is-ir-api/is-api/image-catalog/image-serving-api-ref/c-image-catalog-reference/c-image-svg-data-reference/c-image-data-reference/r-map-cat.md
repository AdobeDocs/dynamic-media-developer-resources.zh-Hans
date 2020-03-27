---
description: 图像映射数据。 没有或更多完整的HTML <AREA>元素，从前到后排序。
seo-description: 图像映射数据。 没有或更多完整的HTML <AREA>元素，从前到后排序。
seo-title: 地图
solution: Experience Manager
title: 地图
topic: Scene7 Image Serving - Image Rendering API
uuid: 674a7a74-91bf-41c4-ab74-a5cb4f8abe1d
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 地图{#map}

图像映射数据。 没有或更多完整 `<AREA>` 的HTML元素，从前到后排序。

服务器将解释并可能更改SHAPE和COORDS属性。 （此版本不支持SHAPE=CIRCLE。）所有其他属性 `<AREA>` 都无需修改即可传递。 使用COORDS属性指定的坐标值必须是未修改的源图像的左上角的像素偏移量。 (`%` 此版本中不支持坐标，可能无法正确处理。)

## 属性 {#section-f52d89fd399b4356ac05277e6c12f956}

文本字符串值。 如果指定，则它必须是一个或多个完整的HTML `<AREA>` 元素。

此字段参与文本字符串本地化。 有关详细 [信息，请参阅](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)*HTTP协议参考中的文本字符串本地化* 。

## 默认 {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

无。

## 另请参阅 {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)，文本字 [符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
