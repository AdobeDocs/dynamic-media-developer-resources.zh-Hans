---
description: 请求模糊化模式。 指定必须应用于有效请求的模糊化类型。
seo-description: 请求模糊化模式。 指定必须应用于有效请求的模糊化类型。
seo-title: 请求模糊化
solution: Experience Manager
title: 请求模糊化
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 07154e06-c386-45a7-b5ac-60f0aef3c362
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 2%

---


# RequestObfuscation{#requestobfuscation}

请求模糊化模式。 指定必须应用于有效请求的模糊化类型。

## 属性 {#section-0819432615324e259f24717e16835427}

枚举。 设置为0可禁用请求模糊处理，设置为1可选择base64编码。 目前不支持任何其他模糊化方法。

## 默认 {#section-e7f49493d9a940acb4f7938df7cac44d}

如果未定义或为空，则从`default::RequestObfuscation`继承。
