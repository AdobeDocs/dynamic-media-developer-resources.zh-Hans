---
description: 为给定的s7 elementID设置任意属性。
solution: Experience Manager
title: setAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---

# setAttr{#setattr}

为给定的s7：elementID设置任意属性。

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

如果FXG节点元素具有 `s7:elementID` 定义，可以处理该节点的属性。 您可以根据需要设置任意数量的属性/值对。 属性不需要在FXG中定义，但它必须对节点元素有效。 介于以下范围中的所有值： `{}` 必须转义。

## 示例 {#section-9c37470d5f0349e5b0a97291782cb7a6}

假设 `s7:elementID="Group1"` 属性是为 `BitmapGraphic` 节点，则以下内容有效：

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

此示例设置 *[!DNL x]*， *[!DNL y]*， *[!DNL rotation]*， *[!DNL scaleX]*、和 *[!DNL scaleY]* 对于 `BitmapGraphic` 和会覆盖任何现有值。
