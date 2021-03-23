---
description: 为s7 elementID设置文本节点值。
seo-description: 为s7 elementID设置文本节点值。
seo-title: setVal
solution: Experience Manager
title: setVal
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '75'
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
