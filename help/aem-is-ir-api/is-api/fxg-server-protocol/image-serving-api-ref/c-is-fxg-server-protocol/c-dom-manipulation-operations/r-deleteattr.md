---
description: 删除给定s7 elementID的任何属性。
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7cecd0aa-c928-4652-a92f-f21ebcf83304
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 2%

---

# deleteAttr{#deleteattr}

删除给定s7：elementID的任何属性。

`deleteAttr.elementID={attributeName%26attributeName}`

如果FXG节点元素具有 `s7:elementID` 定义时，可以使用此命令删除该节点的属性。

## 示例 {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

此示例删除属性 *[!DNL x]*， *[!DNL y]*、和 *[!DNL visible]* 来自原始FXG节点。
