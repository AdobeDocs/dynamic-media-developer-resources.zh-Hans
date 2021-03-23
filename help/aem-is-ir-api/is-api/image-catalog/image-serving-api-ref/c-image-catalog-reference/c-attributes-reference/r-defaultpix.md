---
description: 默认视图大小。
seo-description: 默认视图大小。
seo-title: DefaultPix
solution: Experience Manager
title: DefaultPix
uuid: f5d2e4f7-f9c5-40a5-8a64-67241fcb0242
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---


# DefaultPix{#defaultpix}

默认视图大小。

如果请求未使用`wid=`、`hei=`或`scl=`显式指定视图大小，则服务器将限制返回图像不大于此宽度和高度。

## 属性 {#section-c3e658cf82c540d986b118f74f0fe1b2}

两个整数，0或更大，用逗号分隔。 宽度和高度（以像素为单位）。 可以将任一或两个值设置为0，以保持它们不受约束。

不适用于嵌套/嵌入的请求。

## 默认 {#section-b7338b2bf5114fff83b0714a57b20639}

如果未定义或为空，则从`default::DefaultPix`继承。

## 另请参阅 {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [目录：:MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
