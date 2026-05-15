---
title: setVal
description: 设置s7 elementID的文本节点值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
TQID: 'https://experienceleague.adobe.com/bwE12rWee56rVQDuctPsmq5TUwVJy39HNUff-ZYuybM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 1%

---

# setVal{#setval}

设置s7:elementID的文本节点值。

`setVal.elementID= *[!DNL value]*`

如果FXG节点元素定义了`s7:elementID`，则可以操作该节点的文本值。

## 示例 {#section-f574fd66dedd4a219aa537d7bdabea23}

假定为`TextGraphic`节点定义了`s7:elementID="paragraph1"`特性，则以下内容有效：

`&setVal.paragraph=Hello`

此示例将段落节点的文本值设置为“Hello”。
