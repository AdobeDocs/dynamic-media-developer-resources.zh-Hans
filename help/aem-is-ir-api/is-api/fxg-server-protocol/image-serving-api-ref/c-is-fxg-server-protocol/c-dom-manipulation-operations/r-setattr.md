---
title: setAttr
description: 为给定的s7 elementID设置任意属性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---

# setAttr{#setattr}

为给定的s7：elementID设置任意属性。

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

如果FXG节点元素定义了`s7:elementID`，则可以处理该节点的属性。 您可以根据需要设置任意数量的属性/值对。 属性不需要在FXG中定义，但是它必须对节点元素有效。 `{}`之间的所有值都必须进行转义。

## 示例 {#section-9c37470d5f0349e5b0a97291782cb7a6}

假定为`BitmapGraphic`节点定义了`s7:elementID="Group1"`特性，则以下内容有效：

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

此示例为`BitmapGraphic`设置&#x200B;*[!DNL x]*、*[!DNL y]*、*[!DNL rotation]*、*[!DNL scaleX]*&#x200B;和&#x200B;*[!DNL scaleY]*&#x200B;并覆盖任何现有值。
