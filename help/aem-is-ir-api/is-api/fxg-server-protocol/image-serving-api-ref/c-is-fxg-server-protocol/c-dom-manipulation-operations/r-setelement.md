---
description: 将XML设置为s7 elementID。
seo-description: 将XML设置为s7 elementID。
seo-title: setElement
solution: Experience Manager
title: setElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setElement{#setelement}

将XML设置为s7:elementID。

`setElement.elementID=<XML>`

如果FXG节点元素已定义， `s7:elementID` 则该值将 `<XML>` 作为子元素替换。 The `<XML>` must be encoded.

## 示例 {#section-f23a998b18994dd3b5d4e1965718db9f}

假设为 `s7:elementID="group2"` 节点定义了属性， `Group` 则下列内容有效：

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

此示例从节点中删除所有子 `group2`级，并将其替换为新的子 `TextGraphic` 级节点。
