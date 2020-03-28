---
description: 请求模糊化模式。 指定必须应用于有效请求的模糊处理类型。
seo-description: 请求模糊化模式。 指定必须应用于有效请求的模糊处理类型。
seo-title: 请求模糊处理
solution: Experience Manager
title: 请求模糊处理
topic: Scene7 Image Serving - Image Rendering API
uuid: 07154e06-c386-45a7-b5ac-60f0aef3c362
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 请求模糊处理{#requestobfuscation}

请求模糊化模式。 指定必须应用于有效请求的模糊处理类型。

## 属性 {#section-0819432615324e259f24717e16835427}

枚举。 设置为0可禁用请求模糊处理，设置为1可选择base64编码。 目前不支持任何其他模糊处理方法。

## 默认 {#section-e7f49493d9a940acb4f7938df7cac44d}

如果未定义 `default::RequestObfuscation` 或为空，则从中继承。
