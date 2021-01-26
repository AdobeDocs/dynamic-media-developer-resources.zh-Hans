---
description: 将XML设置为s7 elementID。
seo-description: 将XML设置为s7 elementID。
seo-title: setElement
solution: Experience Manager
title: setElement
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 1%

---


# setElement{#setelement}

将XML设置为s7:elementID。

`setElement.elementID=<XML>`

如果FXG节点元素定义了`s7:elementID`，则`<XML>`值将替换为子元素。 `<XML>`必须进行编码。

## 示例 {#section-f23a998b18994dd3b5d4e1965718db9f}

假定为`Group`节点定义了`s7:elementID="group2"`属性，则以下属性有效：

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

此示例从`group2`节点中删除所有子节点，并用新的`TextGraphic`子节点替换它。
