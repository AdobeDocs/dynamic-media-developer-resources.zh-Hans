---
title: 混合模式
description: 混合模式。 指定合成图层时使用的混合类型。 模拟Photoshop中可用的常用混合模式。 有关详细信息，请参阅Photoshop文档。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f0b8b0a-a8ac-4932-986c-5d14d3311f1b
TQID: 'https://experienceleague.adobe.com/cH4BuvInJjio0siCV6GD8rx8nAI-pPkmgqiQN-xZ47I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 67
ht-degree: 5%

---

# 混合模式{#blendmode}

混合模式。 指定合成图层时使用的混合类型。 模拟Photoshop中可用的常用混合模式。 有关详细信息，请参阅Photoshop文档。

`blendMode=norm|dissolve|lighten|darken|mult|screen`

## 属性 {#section-418aad5a417f49929d1953e226e5c8dd}

层属性。 已被`layer=0`和`layer=comp`忽略。

## 默认 {#section-69829acc6532448d8612a4a54e86f00e}

`blendMode=norm`

## 示例 {#section-d209dd9c270b469c87558a8910c50b61}

`…&size=200,200&bgColor=191,120,241&…`

`…&layer=1&src=myRootId/myImageId&opac=80&blendMode=dissolve&…`

## 另请参阅 {#section-bc7ccdfcb310441c938c0bde3e00d7b3}

[opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)
