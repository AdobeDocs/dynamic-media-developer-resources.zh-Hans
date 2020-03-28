---
description: 启用合成字体变体。 控制服务器应生成错误响应，还是在请求了粗体、斜体或粗体／斜体字体样式但在字体映射中找不到该样式时合成该样式。
seo-description: 启用合成字体变体。 控制服务器应生成错误响应，还是在请求了粗体、斜体或粗体／斜体字体样式但在字体映射中找不到该样式时合成该样式。
seo-title: SyntherizeFontStyles
solution: Experience Manager
title: SyntherizeFontStyles
topic: Scene7 Image Serving - Image Rendering API
uuid: f1c67490-7f14-4a6c-a7ba-5a476231ef34
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SyntherizeFontStyles{#synthesizefontstyles}

启用合成字体变体。 控制服务器应生成错误响应，还是在请求了粗体、斜体或粗体／斜体字体样式但在字体映射中找不到该样式时合成该样式。

>[!NOTE]
>
>合成字体样式通常会导致渲染质量低于对此类样式使用实际字体。

## 属性 {#section-3205560a74774ebf9c916b07bd15aca6}

标记. 设置为0可禁用，设置为1可启用合成字体样式。

## 默认 {#section-71f94aa65e404d14b441674c040b59e3}

如果未定义 `default::SynthesizeFontStyles` 或为空，则从中继承。

## 另请参阅 {#section-47a79659cc844272b6d5f36c946e12ac}

[字体映射参考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)
