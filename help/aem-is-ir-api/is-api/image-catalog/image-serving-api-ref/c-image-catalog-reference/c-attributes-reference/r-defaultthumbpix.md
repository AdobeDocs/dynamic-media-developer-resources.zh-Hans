---
description: 默认缩略图大小。 用于缩览图请求(req=tmb)，而不是属性DefaultPix。
solution: Experience Manager
title: DefaultThumbPix
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# DefaultThumbPix{#defaultthumbpix}

默认缩略图大小。 Useded而不是attribute::DefaultPix for thumbnail requests(req=tmb)。

如果缩略图请求(`req=tmb`)未明确指定大小，而未使用`wid=`、`hei=`或`scl=`显式指定视图大小，则服务器将限制返回图像不大于此宽度和高度。

## 属性 {#section-650d9b1194fb4c47a03c6809e6b4af0e}

两个整数，0或更大，用逗号分隔。 宽度和高度（以像素为单位）。 可以将任一或两个值设置为0，以保持它们不受约束。

不适用于嵌套/嵌入的请求。

## 默认 {#section-2c4a4f14540449638822913513170ff1}

如果未定义或为空，则从`default::DefaultThumbPix`继承。

## 另请参阅 {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [属性：:DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
