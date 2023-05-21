---
description: 設定s7 elementID的文位元組點值。
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 1%

---

# setVal{#setval}

設定s7：elementID的文位元組點值。

`setVal.elementID= *[!DNL value]*`

如果FXG節點元素具有 `s7:elementID` 定義時，可以操作該節點的文字值。

## 示例 {#section-f574fd66dedd4a219aa537d7bdabea23}

假設 `s7:elementID="paragraph1"` 屬性已為 `TextGraphic` 節點，則以下內容有效：

`&setVal.paragraph=Hello`

此範例將段落節點的文字值設為「Hello」。
