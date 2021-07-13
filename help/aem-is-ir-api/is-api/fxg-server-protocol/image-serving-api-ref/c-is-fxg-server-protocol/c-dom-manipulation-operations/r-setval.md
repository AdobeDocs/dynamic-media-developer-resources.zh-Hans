---
description: 为s7 elementID设置文本节点值。
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '64'
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
