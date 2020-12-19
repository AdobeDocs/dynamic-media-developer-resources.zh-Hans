---
description: 为s7 elementID设置文本节点值。
seo-description: 为s7 elementID设置文本节点值。
seo-title: setVal
solution: Experience Manager
title: setVal
topic: Scene7 Image Serving - Image Rendering API
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---


# setVal{#setval}

为s7:elementID设置文本节点值。

`setVal.elementID= *[!DNL value]*`

如果FXG节点元素定义了`s7:elementID`，则可以处理该节点的文本值。

## 示例 {#section-f574fd66dedd4a219aa537d7bdabea23}

假定为`TextGraphic`节点定义了`s7:elementID="paragraph1"`属性，则以下属性有效：

`&setVal.paragraph=Hello`

此示例将段落节点的文本值设置为“Hello”。
