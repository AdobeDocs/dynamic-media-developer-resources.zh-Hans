---
title: 解析模式
description: 重新取样模式。 resMode=的默认值。 指定用于将渲染的图像缩放到最终大小的重新取样和插值属性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c57932a0-529c-4f31-b60e-a38de6fe277f
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 4%

---

# 解析模式{#resmode}

重新取样模式。 `resMode=`的默认值。 指定用于将渲染的图像缩放到最终大小的重新取样和插值属性。

## 属性 {#section-1183a155f33c4eca80f1dc6fb6bda1b5}

枚举。 对于`'bilin'`，设置为2；对于`'bicub'`，设置为3；对于`'sharp2'`插值模式，设置为4（有关详细信息，请参阅[resMode=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md)）。

## 默认 {#section-ed432a0acc3e4bce926a07e9cfd2c865}

如果未定义或为空，则从`default::ResMode`继承。

## 另请参阅 {#section-34b71c295b4349dfb4379823a2de83c2}

[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
