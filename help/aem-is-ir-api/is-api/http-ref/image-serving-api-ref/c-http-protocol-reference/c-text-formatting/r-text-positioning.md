---
title: 文本定位
description: 当应用于预先设置的图层时（即同时指定了size=时），text=渲染器会放置与textPs=渲染器截然不同的文本。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# 文本定位{#text-positioning}

此 `text=` 当应用于预先设置的图层时（即同时指定了size=时），渲染器定位的文本与textPs=渲染器截然不同。

自定大小 `text=`和 `textPs=` 图层具有相似的外观和位置。

此 `textPs=` 将字符单元格的顶部与文本框的顶部对齐(假设 `\vertalt`)，即使这会导致部分渲染的文本字形部分延伸到文本框边界之外。 某些字体的渲染字形也可能稍微突出超出文本框的左右边缘。 对于要求所有渲染的文本都包含在图层矩形内的应用程序，RTF `\marg*` 命令或 `textFlowPath=` 可用于调整文本渲染区域。

相比之下， `text=` 根据需要移动渲染的文本，并确保所有渲染的字形完全适合指定的文本框。

同时 `text=` 对于简单应用程序可能使用起来会略微简单一些， `textPs=` 提供独立于字体表面和文本效果的精确定位。

## 示例 {#section-1b6bdf2ea34447528188ae4e1430ee71}

以下示例适用于预先调整大小的文本。 自调整文本大小的行为不同。

** `Text=` 始终在顶部提供窄边距：**

![文本定位示例一个图像](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` 呈现文本与文本框顶部紧密对齐，这会导致轻微剪切，即使对于Arial®：**等常见字体也是如此

![文本定位示例二图像](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` 自动将渲染的文本下移以避免剪切：**

![文本定位示例三图像](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` 不移动包含凸起部分的文本，如果文本位于图层0：**上，则会导致明显的裁剪

![文本定位示例四图像](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**顶部的10 pt (200 twips)边距表示此文本而不进行剪切：**

![文本定位示例五幅图像](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**某些脚本字体的渲染字形可能会显着延伸到文本框之外：**

![文本定位示例六幅图像](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
