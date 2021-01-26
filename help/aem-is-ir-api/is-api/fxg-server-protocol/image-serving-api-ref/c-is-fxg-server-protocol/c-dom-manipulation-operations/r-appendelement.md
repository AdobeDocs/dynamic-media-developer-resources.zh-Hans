---
description: 将XML追加到s7 elementID。
seo-description: 将XML追加到s7 elementID。
seo-title: appendElement
solution: Experience Manager
title: appendElement
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 062c8288-4517-42a1-9f9f-f3c7bbb4b63b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 1%

---


# appendElement{#appendelement}

将XML追加到s7:elementID。

`appendElement.elementID=<XML>`

如果FXG节点元素定义了`s7:elementID`，则将`<XML>`值附加为子元素。 `<XML>`必须进行编码。

## 示例 {#section-4368570aa198485d91b73b4d0741478f}

假设为组节点定义了`s7:elementID="group1"`属性，则以下属性有效：

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

此示例向`group1`附加一个文本图形子项。
