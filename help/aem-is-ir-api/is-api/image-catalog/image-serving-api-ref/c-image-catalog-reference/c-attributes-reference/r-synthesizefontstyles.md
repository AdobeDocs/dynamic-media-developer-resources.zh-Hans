---
title: SynthesizeFontStyles
description: 启用合成字体变量。 控制当请求了粗体、斜体或粗体/斜体字体样式但在字体映射中找不到时，服务器应生成错误响应还是合成此类样式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08f20748-71c7-4b9f-9b45-70352f9abf35
TQID: 'https://experienceleague.adobe.com/E5yyjiqiPxEbLecNDw5HIa3dJ9XqyGa3Ipys4EtancU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 2%

---

# SynthesizeFontStyles{#synthesizefontstyles}

启用合成字体变量。 控制当请求了粗体、斜体或粗体/斜体字体样式但在字体映射中找不到时，服务器应生成错误响应还是合成此类样式。

>[!NOTE]
>
>合成字体样式通常会导致渲染质量低于对此类样式使用实际字体。

## 属性 {#section-3205560a74774ebf9c916b07bd15aca6}

标志。 设置为0可禁用合成字体样式，设置为1可启用合成字体样式。

## 默认 {#section-71f94aa65e404d14b441674c040b59e3}

如果未定义或为空，则从`default::SynthesizeFontStyles`继承。

## 另请参阅 {#section-47a79659cc844272b6d5f36c946e12ac}

[字体映射引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)
