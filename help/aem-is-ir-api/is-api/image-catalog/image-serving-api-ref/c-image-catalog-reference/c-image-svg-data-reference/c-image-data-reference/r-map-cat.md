---
description: 图像映射数据。 没有或更完整的HTML<AREA>元素，从前到后排序。
solution: Experience Manager
title: 地图
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 4%

---

# 地图{#map}

图像映射数据。 没有或更完整的HTML`<AREA>`元素，从前到后排序。

服务器将解释并可能更改SHAPE和COORDS属性（此版本不支持SHAPE=CIRCLE）。 `<AREA>`的所有其他属性无需修改即可传递。 使用COORDS属性指定的坐标值必须是未修改源图像左上角的像素偏移。 （`%`坐标在此版本中不受支持，可能无法正确处理。）

## 属性 {#section-f52d89fd399b4356ac05277e6c12f956}

文本字符串值。 如果指定，则必须是一个或多个完整的HTML`<AREA>`元素。

此字段参与文本字符串本地化。 有关详细信息，请参阅&#x200B;*HTTP协议引用*&#x200B;中的[文本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)。

## 默认 {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

无。

## 另请参阅 {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) ， [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)， [文本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
