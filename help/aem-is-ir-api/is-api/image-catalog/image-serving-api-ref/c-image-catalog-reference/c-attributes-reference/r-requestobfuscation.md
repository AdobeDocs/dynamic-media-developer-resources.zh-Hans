---
description: 请求模糊处理模式。 指定必须应用于有效请求的模糊处理类型。
solution: Experience Manager
title: 请求模糊处理
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 2%

---


# RequestObfuscation{#requestobfuscation}

请求模糊处理模式。 指定必须应用于有效请求的模糊处理类型。

## 属性 {#section-0819432615324e259f24717e16835427}

枚举。 设置为0可禁用请求模糊处理，设置为1可选择base64编码。 此时不支持其他混淆方法。

## 默认 {#section-e7f49493d9a940acb4f7938df7cac44d}

如果未定义或为空，则从`default::RequestObfuscation`继承。
