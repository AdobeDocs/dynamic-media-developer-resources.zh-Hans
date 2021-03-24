---
description: 删除给定s7 elementID的任何属性。
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 1%

---


# deleteAttr{#deleteattr}

删除给定s7:elementID的任何属性。

`deleteAttr.elementID={attributeName%26attributeName}`

如果FXG节点元素定义了`s7:elementID`，则可以使用此命令删除该节点的属性。

## 示例 {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

此示例从原始FXG节点中删除属性&#x200B;*[!DNL x]*、*[!DNL y]*&#x200B;和&#x200B;*[!DNL visible]*。
