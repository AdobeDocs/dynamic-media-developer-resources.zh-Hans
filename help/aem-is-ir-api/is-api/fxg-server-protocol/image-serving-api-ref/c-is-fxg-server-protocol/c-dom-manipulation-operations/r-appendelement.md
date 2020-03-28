---
description: 将XML追加到s7 elementID。
seo-description: 将XML追加到s7 elementID。
seo-title: appendElement
solution: Experience Manager
title: appendElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 062c8288-4517-42a1-9f9f-f3c7bbb4b63b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# appendElement{#appendelement}

将XML追加到s7:elementID。

`appendElement.elementID=<XML>`

如果FXG节点元素已定义， `s7:elementID` 则该值将 `<XML>` 作为子元素附加。 The `<XML>` must be encoded.

## 示例 {#section-4368570aa198485d91b73b4d0741478f}

假设为 `s7:elementID="group1"` 组节点定义了属性，则以下内容有效：

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

此示例向附加一个文本图形子项 `group1`。
