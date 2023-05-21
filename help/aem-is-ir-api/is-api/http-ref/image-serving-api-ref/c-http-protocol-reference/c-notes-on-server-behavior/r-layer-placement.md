---
title: 圖層位置
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# 圖層位置{#layer-placement}

將圖層原點(origin=)與背景圖層原點對齊於pos=所指定的位移來定點陣圖層。

如果未明確指定影像圖層的圖層原點，則計算方式如下：

1. 決定影像錨點。 使用 `anchor=`、或（若未指定） `catalog::Anchor`.
1. 如果已定義影像錨點，請套用圖層變形和 `extend=` 將其轉換為origin=值。
1. 如果未定義影像錨點，圖層原點會放置在圖層矩形的中心（套用後） `extend=`)。

![圖層位置影像](assets/layerplacement.png)
