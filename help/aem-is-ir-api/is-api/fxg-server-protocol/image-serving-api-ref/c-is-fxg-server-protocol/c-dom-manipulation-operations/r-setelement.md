---
description: 將XML設為s7 elementID。
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

將XML設為s7：elementID。

`setElement.elementID=<XML>`

如果FXG節點元素具有 `s7:elementID` 已定義， `<XML>` 值會取代為子元素。 此 `<XML>` 必須編碼。

## 示例 {#section-f23a998b18994dd3b5d4e1965718db9f}

假設 `s7:elementID="group2"` 屬性已為 `Group` 節點，則以下內容有效：

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

此範例會移除 `group2`節點並以新節點取代 `TextGraphic` 子節點。
