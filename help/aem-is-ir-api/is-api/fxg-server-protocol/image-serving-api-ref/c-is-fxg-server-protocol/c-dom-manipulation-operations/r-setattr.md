---
description: 为给定的s7元素ID设置任何属性。
seo-description: 为给定的s7元素ID设置任何属性。
seo-title: setAttr
solution: Experience Manager
title: setAttr
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 968f7496-3cd4-4670-96fc-53127bba9a83
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---


# setAttr{#setattr}

为给定的s7:elementID设置任何属性。

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

如果FXG节点元素定义了`s7:elementID`，则可以处理该节点的属性。 您可以根据需要设置任意多个属性／值对。 属性无需在FXG中定义，但对于节点元素必须有效。 `{}`之间的所有值都必须为“转义”。

## 示例 {#section-9c37470d5f0349e5b0a97291782cb7a6}

假定为`BitmapGraphic`节点定义了`s7:elementID="Group1"`属性，则以下属性有效：

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

此示例设置`BitmapGraphic`的&#x200B;*[!DNL x]*、*[!DNL y]*、*[!DNL rotation]*、*[!DNL scaleX]*&#x200B;和&#x200B;*[!DNL scaleY]*，并覆盖任何现有值。
