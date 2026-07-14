---
title: 默认像素
description: 默认渲染图像大小。 如果请求未使用wid=或hei=明确指定视图大小，服务器将限制回复图像不超过此宽度和高度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
TQID: 'https://experienceleague.adobe.com/n0m-j--YSFkdFmNOuJhRi3az-tARnc-N3sRmgkSJryE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 2%

---

# 默认像素{#defaultpix}

默认渲染图像大小。 如果请求未使用wid=或hei=明确指定视图大小，服务器将限制回复图像不超过此宽度和高度。

## 属性 {#section-9dc5474fc75842308796ab6440b29611}

0或更大的两个整数，用逗号分隔。 宽度和高度（像素）。 可以将任一值或两个值都设置为0以使其不受约束。

不适用于嵌套/嵌入的请求。

## 默认 {#section-1935781c561e4679aa87a5bcced8df90}

如果未定义或为空，则从`default::DefaultPix`继承。

## 另请参阅 {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ，[hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)，[attribute：：MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)

