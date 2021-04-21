---
description: 为s7 elementID设置文本节点值。
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---


# setVal{#setval}

为s7:elementID设置文本节点值。

`setVal.elementID= *[!DNL value]*`

如果FXG节点元素定义了`s7:elementID`，则可以处理该节点的文本值。

## 示例 {#section-f574fd66dedd4a219aa537d7bdabea23}

假设为`TextGraphic`节点定义了`s7:elementID="paragraph1"`属性，则以下属性有效：

`&setVal.paragraph=Hello`

此示例将段落节点的文本值设置为“Hello”。
