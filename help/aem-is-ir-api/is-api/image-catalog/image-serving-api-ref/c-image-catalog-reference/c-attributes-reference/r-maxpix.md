---
description: 回复图像大小限制。 可返回到客户端的最大回复图像宽度和高度。
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
TQID: 'https://experienceleague.adobe.com/lX4ooC7B0VIJDRr0yZJVmp45qnXbSuimMZSyU9rWLcw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 3%

---

# MaxPix{#maxpix}

回复图像大小限制。 可返回到客户端的最大回复图像宽度和高度。

如果请求会导致回复图像的宽度或高度大于`attribute::MaxPix`，则服务器返回错误。

## 属性 {#section-b175425b9e9f48e0b1a71640f6a9e936}

两个大于0的整数，用逗号分隔。 宽度和高度（像素）。 也可以设置为`0,0`以允许使用任意回复图像大小而没有任何限制。

## 默认 {#section-1003537434da432fb2af100ecdbf9d72}

如果未定义或为空，则从`default::MaxPix`继承。

## 另请参阅 {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ， [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
