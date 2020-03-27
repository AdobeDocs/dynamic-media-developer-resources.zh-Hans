---
description: 为给定的s7 elementID设置任何属性。
seo-description: 为给定的s7 elementID设置任何属性。
seo-title: setAttr
solution: Experience Manager
title: setAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: 968f7496-3cd4-4670-96fc-53127bba9a83
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAttr{#setattr}

为给定的s7:elementID设置任何属性。

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

如果FXG节点元素已定义， `s7:elementID` 则可以操作该节点的属性。 您可以根据需要设置任意数量的属性／值对。 属性无需在FXG中定义，但对于节点元素必须有效。 介于这两个值之间 `{}` 的所有值都必须转义。

## 示例 {#section-9c37470d5f0349e5b0a97291782cb7a6}

假设为 `s7:elementID="Group1"` 某个节点定义了属 `BitmapGraphic` 性，则以下内容有效：

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

此示例设置 *[!DNL x]*、、、 *[!DNL y]*&#x200B;和的 *[!DNL rotation]*&#x200B;和，并 *[!DNL scaleX]*&#x200B;覆盖任 *[!DNL scaleY]*`BitmapGraphic` 何现有值。
