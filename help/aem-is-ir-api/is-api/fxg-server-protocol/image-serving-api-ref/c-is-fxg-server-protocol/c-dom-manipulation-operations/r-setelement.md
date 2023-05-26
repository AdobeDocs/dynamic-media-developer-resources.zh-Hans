---
description: 将XML设置为s7 elementID。
solution: Experience Manager
title: setElement
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---

# setElement{#setelement}

将XML设置为s7：elementID。

`setElement.elementID=<XML>`

如果FXG节点元素具有 `s7:elementID` 已定义， `<XML>` 值将被替换为一个子元素。 此 `<XML>` 必须经过编码。

## 示例 {#section-f23a998b18994dd3b5d4e1965718db9f}

假设 `s7:elementID="group2"` 属性是为 `Group` 节点，则以下内容有效：

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

此示例从 `group2`节点并将其替换为新的 `TextGraphic` 子节点。
