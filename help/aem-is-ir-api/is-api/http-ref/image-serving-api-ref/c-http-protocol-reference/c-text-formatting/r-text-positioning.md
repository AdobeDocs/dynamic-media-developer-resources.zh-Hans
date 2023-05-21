---
title: 文字定位
description: 在套用至預先設定的大小圖層時（亦即指定size=時），text=轉譯器會定位與textPs=轉譯器截然不同的文字。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# 文字定位{#text-positioning}

此 `text=` 當套用至預先設定的大小圖層時（亦即指定size=時），轉譯器會定位與textPs=轉譯器截然不同的文字。

自行調整大小 `text=`和 `textPs=` 圖層具有類似的外觀和位置。

此 `textPs=` 將字元儲存格的頂端與文字方塊的頂端對齊(假設 `\vertalt`)，即使這會導致部分呈現的文字字元延伸到文字方塊邊界之外。 某些字型的演算字元也可能會稍微超出文字方塊的左右邊緣。 對於要求所有演算後的文字都包含在圖層矩形內的應用程式，RTF會 `\marg*` 命令或 `textFlowPath=` 可用來調整文字演算區域。

相反地， `text=` 視需要移動演算後的文字，並確保所有演算後的字元完全符合指定的文字方塊。

當 `text=` 對於簡單的應用程式可能更容易使用， `textPs=` 提供獨立於字型面和文字效果的精確定位。

## 示例 {#section-1b6bdf2ea34447528188ae4e1430ee71}

以下範例適用於預先調整大小的文字。 自行調整文字大小的行為不同。

** `Text=` 一律會在頂端提供窄邊界：**

![文字定位範例一個影像](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` 會呈現文字與文字方塊頂端緊密對齊，因此會產生輕微的剪裁，即使是Arial®：**等常見字型也是如此

![文字定位範例二影像](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` 自動將演算後的文字下移以避免剪裁：**

![文字定位範例三影像](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` 不會移動包含凸出部分的文字，如果文字位於圖層0：**上，則會產生顯著的剪裁

![文字定位範例四影像](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**頂端的10點（200倍）邊界會轉譯此文字而不進行剪裁：**

![文字定位範例五影像](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**某些指令碼字型的演算字元可能會顯著延伸至文字方塊之外：**

![文字定位範例六影像](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
