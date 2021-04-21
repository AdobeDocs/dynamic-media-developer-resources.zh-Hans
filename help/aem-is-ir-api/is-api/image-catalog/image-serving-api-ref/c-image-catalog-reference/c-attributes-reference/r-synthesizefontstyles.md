---
description: 启用合成字体变量。 控制如果请求了某种样式，但在字体映射中找不到该样式，则服务器是否应生成错误响应或合成粗体、斜体或粗体/斜体字体样式。
solution: Experience Manager
title: SynthesizeFontStyles
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# SynthesizeFontStyles{#synthesizefontstyles}

启用合成字体变量。 控制如果请求了某种样式，但在字体映射中找不到该样式，则服务器是否应生成错误响应或合成粗体、斜体或粗体/斜体字体样式。

>[!NOTE]
>
>合成字体样式通常会导致此类样式的渲染质量低于使用实际字体。

## 属性 {#section-3205560a74774ebf9c916b07bd15aca6}

标记. 设置为0可禁用，设置为1可启用合成字体样式。

## 默认 {#section-71f94aa65e404d14b441674c040b59e3}

如果未定义或为空，则从`default::SynthesizeFontStyles`继承。

## 另请参阅 {#section-47a79659cc844272b6d5f36c946e12ac}

[字体映射参考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)
