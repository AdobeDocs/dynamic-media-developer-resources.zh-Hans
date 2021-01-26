---
description: 混合模式. 指定合成图层时使用的混合类型。 模拟Photoshop的常用混合模式。 有关详细信息，请参阅Photoshop文档。
seo-description: 混合模式. 指定合成图层时使用的混合类型。 模拟Photoshop的常用混合模式。 有关详细信息，请参阅Photoshop文档。
seo-title: blendMode
solution: Experience Manager
title: blendMode
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9ae30495-c10b-4c55-968e-effb602a0857
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 14%

---


# blendMode{#blendmode}

混合模式. 指定合成图层时使用的混合类型。 模拟Photoshop的常用混合模式。 有关详细信息，请参阅Photoshop文档。

`blendMode=norm|dissolve|lighten|darken|mult|screen`

## 属性 {#section-418aad5a417f49929d1953e226e5c8dd}

图层属性。 被`layer=0`和`layer=comp`忽略。

## 默认 {#section-69829acc6532448d8612a4a54e86f00e}

`blendMode=norm`

## 示例 {#section-d209dd9c270b469c87558a8910c50b61}

`…&size=200,200&bgColor=191,120,241&…`

`…&layer=1&src=myRootId/myImageId&opac=80&blendMode=dissolve&…`

## 另请参阅 {#section-bc7ccdfcb310441c938c0bde3e00d7b3}

[opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)
