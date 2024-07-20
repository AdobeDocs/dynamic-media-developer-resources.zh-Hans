---
title: 文本定位
description: 当应用于预先设置的图层时（即同时指定了size=时），text=渲染器会放置与textPs=渲染器截然不同的文本。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# 文本定位{#text-positioning}

当应用于预先设置的图层时（即同时指定了size=时），`text=`呈现器定位的文本与textPs=呈现器截然不同。

自调整大小的`text=`和`textPs=`图层具有相似的外观和位置。

`textPs=`将字符单元格的顶部与文本框的顶部对齐（假设为`\vertalt`），即使它导致部分呈现的文本字形延伸到文本框边界之外。 某些字体的渲染字形也可能稍微突出超出文本框的左右边缘。 对于要求所有渲染的文本都包含在图层矩形内的应用程序，可以使用RTF `\marg*`命令或`textFlowPath=`来调整文本渲染区域。

相反，`text=`会根据需要移动渲染的文本，并确保所有渲染的字形完全适合指定的文本框。

虽然`text=`对于简单的应用程序可能更容易使用，但`textPs=`提供了独立于字体和文本效果的精确定位。

## 示例 {#section-1b6bdf2ea34447528188ae4e1430ee71}

以下示例适用于预先调整大小的文本。 自调整文本大小的行为不同。

** `Text=`始终在顶部提供窄边距：**

![文本定位示例一个图像](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=`呈现文本与文本框顶部紧密对齐，这会导致轻微剪切，即使对于Arial®：**等常见字体也是如此

![文本定位示例2图像](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=`自动将渲染的文本下移以避免剪切：**

![文本定位示例三张图像](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=`不移动包含凸起部分的文本，如果文本位于图层0：**上，则会导致显着剪切

![文本定位示例4图像](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

顶部的&#x200B;**10 pt (200 twips)的边距在不剪切的情况下呈现此文本：**

![文本定位示例5个图像](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**某些脚本字体的呈现字形可能会显着延伸到文本框之外：**

![文本定位示例6图像](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
