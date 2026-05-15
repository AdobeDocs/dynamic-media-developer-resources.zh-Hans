---
title: 图层放置
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
TQID: https://experienceleague.adobe.com/SMf4V0AmxYIi0o0FZhMkRx9pprIxjJjEcCWT2agF1Bo
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 0f5947b3f28ba40cd479df463c843f7e99155d5e
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 0%

---

# 图层放置{#layer-placement}

通过以pos=指定的偏移将图层原点(origin=)与背景图层原点对齐来定位图层。

如果没有为图像图层明确指定图层原点，则计算如下内容：

1. 确定图像锚点。 使用`anchor=`，如果未指定，则使用`catalog::Anchor`。
1. 如果定义了图像锚点，则应用图层转换和`extend=`以将其转换为origin=值。
1. 如果未定义图像锚点，图层原点将放置在图层矩形的中心（应用`extend=`后）。

![图层位置图像](assets/layerplacement.png)
