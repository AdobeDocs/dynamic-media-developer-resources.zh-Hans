---
description: 設定指定s7 elementID的任何屬性。
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

為指定的s7：elementID設定任何屬性。

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

如果FXG節點元素具有 `s7:elementID` 定義，您可以操作該節點的屬性。 您可以視需要設定多個屬性/值組。 屬性不需要在FXG中定義，但是它必須對節點元素有效。 介於兩者之間的所有值 `{}` 必須逸出。

## 示例 {#section-9c37470d5f0349e5b0a97291782cb7a6}

假設 `s7:elementID="Group1"` 屬性已為 `BitmapGraphic` 節點，則以下為有效：

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

此範例會設定 *[!DNL x]*， *[!DNL y]*， *[!DNL rotation]*， *[!DNL scaleX]*、和 *[!DNL scaleY]* 的 `BitmapGraphic` 和會覆寫任何現有值。
