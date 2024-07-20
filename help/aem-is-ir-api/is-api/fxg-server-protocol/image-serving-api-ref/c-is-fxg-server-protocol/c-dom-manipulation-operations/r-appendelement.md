---
title: appendElement
description: 将XML附加到s7 elementID。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 1%

---

# appendElement{#appendelement}

将XML附加到s7：elementID。

`appendElement.elementID=<XML>`

如果FXG节点元素定义了`s7:elementID`，则`<XML>`值将作为子元素附加。 必须对`<XML>`进行编码。

## 示例 {#section-4368570aa198485d91b73b4d0741478f}

假定为组节点定义了`s7:elementID="group1"`特性，则以下内容有效：

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

此示例将文本图形子项附加到`group1`。
