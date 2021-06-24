---
description: 启用合成字体变量。 控制如果请求了此样式，但在字体映射中找不到该样式，则服务器是否应生成错误响应或合成粗体、斜体或粗体/斜体字体样式。
solution: Experience Manager
title: SyntherizationFontStyles
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 08f20748-71c7-4b9f-9b45-70352f9abf35
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---

# SyntherizationFontStyles{#synthesizefontstyles}

启用合成字体变量。 控制如果请求了此样式，但在字体映射中找不到该样式，则服务器是否应生成错误响应或合成粗体、斜体或粗体/斜体字体样式。

>[!NOTE]
>
>合成字体样式通常会导致渲染质量低于对此类样式使用实际字体。

## 属性 {#section-3205560a74774ebf9c916b07bd15aca6}

标记. 将设置为0禁用，将设置为1启用合成字体样式。

## 默认 {#section-71f94aa65e404d14b441674c040b59e3}

从`default::SynthesizeFontStyles`继承（如果未定义或为空）。

## 另请参阅 {#section-47a79659cc844272b6d5f36c946e12ac}

[字体映射引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)
