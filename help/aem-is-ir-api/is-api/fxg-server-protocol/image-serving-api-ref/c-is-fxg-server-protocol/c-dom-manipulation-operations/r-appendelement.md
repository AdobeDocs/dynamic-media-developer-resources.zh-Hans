---
description: 将XML附加到s7 elementID。
solution: Experience Manager
title: appendElement
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 1%

---

# appendElement{#appendelement}

将XML附加到s7：elementID。

`appendElement.elementID=<XML>`

如果FXG节点元素具有 `s7:elementID` 已定义， `<XML>` 值将作为子元素附加。 此 `<XML>` 必须经过编码。

## 示例 {#section-4368570aa198485d91b73b4d0741478f}

假设 `s7:elementID="group1"` 为组节点定义了属性，则以下内容有效：

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

此示例将一个文本图形子级附加到 `group1`.
