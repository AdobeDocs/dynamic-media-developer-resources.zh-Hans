---
title: setVal
description: 设置s7 elementID的文本节点值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 1%

---

# setVal{#setval}

设置s7:elementID的文本节点值。

`setVal.elementID= *[!DNL value]*`

如果FXG节点元素定义了`s7:elementID`，则可以操作该节点的文本值。

## 示例 {#section-f574fd66dedd4a219aa537d7bdabea23}

假定为`s7:elementID="paragraph1"`节点定义了`TextGraphic`特性，则以下内容有效：

`&setVal.paragraph=Hello`

此示例将段落节点的文本值设置为“Hello”。
