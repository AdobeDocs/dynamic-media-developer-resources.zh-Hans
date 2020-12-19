---
description: 当应用于预定大小的图层时，text= renderer定位的文本与textPs= renderer基本不同（即，当也指定了size=时）。
seo-description: 当应用于预定大小的图层时，text= renderer定位的文本与textPs= renderer基本不同（即，当也指定了size=时）。
seo-title: 文本定位
solution: Experience Manager
title: 文本定位
topic: Scene7 Image Serving - Image Rendering API
uuid: 77289c50-2f3a-4486-8274-eecfd6e5452f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---


# 文本定位{#text-positioning}

当应用于预定大小的图层时，text= renderer定位的文本与textPs= renderer基本不同（即，当也指定了size=时）。

自调整大小`text=`和`textPs=`图层的外观和位置相似。

`textPs=` 将字符单元格的顶部与文本框的顶部对齐(假定 `\vertalt`)，即使这会导致部分渲染的文本字形部分扩展到文本框边界之外。某些字体的渲染字形也可能略微突出到文本框的左右边缘之外。 对于要求图层矩形中包含所有渲染文本的应用程序，可以使用RTF `\marg*`命令或`textFlowPath=`来调整文本渲染区域。

相反，`text=`将根据需要移动渲染的文本，并确保所有渲染的字形完全适合指定文本框。

虽然`text=`对于简单的应用程序可能略为简单，但`textPs=`优惠的精确定位与字体和文本效果无关。

## 示例 {#section-1b6bdf2ea34447528188ae4e1430ee71}

以下示例适用于预定大小的文本。 自行调整文本大小的行为不同。

** `Text=`始终在顶部提供窄边距：**

![](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=`呈现文本与文本框顶部紧密对齐，这可能导致轻微裁切，即使对于Arial等常见字体也是如此：**

![](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=`将自动将渲染的文本向下移动以避免裁切：**

![](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=`不会移动包含凸起部分的文本，如果文本位于图层0上，则会出现显着的剪切：**

![](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**顶部的10 pt(200 twips)边距可呈现此文本，而无需进行剪切：**

![](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**某些脚本字体的呈现字形可能会显着扩展到文本框之外：**

![](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
