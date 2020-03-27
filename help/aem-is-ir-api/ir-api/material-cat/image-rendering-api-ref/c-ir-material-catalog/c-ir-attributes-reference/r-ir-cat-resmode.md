---
description: 重新取样模式。 resMode=的默认值。 指定用于将渲染的图像缩放到最终大小的重新取样属性和插值属性。
seo-description: 重新取样模式。 resMode=的默认值。 指定用于将渲染的图像缩放到最终大小的重新取样属性和插值属性。
seo-title: ResMode
solution: Experience Manager
title: ResMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 91d83274-b3e1-4233-bd01-21936726e1db
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ResMode{#resmode}

重新取样模式。 resMode=的默认值。 指定用于将渲染的图像缩放到最终大小的重新取样属性和插值属性。

## 属性 {#section-1183a155f33c4eca80f1dc6fb6bda1b5}

枚举。 对于插值模式， `'bilin'`设置为2表示 `'bicub'`，设置为3表示，或设置为4 `'sharp2'` 表示(有关详细信息， ` [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)` 请参阅)。

## 默认 {#section-ed432a0acc3e4bce926a07e9cfd2c865}

如果未定义 `default::ResMode` 或为空，则从中继承。

## 另请参阅 {#section-34b71c295b4349dfb4379823a2de83c2}

[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
