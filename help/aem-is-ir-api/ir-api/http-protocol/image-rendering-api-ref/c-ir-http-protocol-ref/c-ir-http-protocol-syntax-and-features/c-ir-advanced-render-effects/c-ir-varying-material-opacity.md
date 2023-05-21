---
title: 不同材質不透明度
description: 實色和套用至重疊物件的可重複紋理，以及貼花和視窗遮蓋材料都支援可變不透明度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 不同材質不透明度{#varying-material-opacity}

實色和套用至重疊物件的可重複紋理，以及貼花和視窗遮蓋材料都支援可變不透明度。

只要使用具有Alpha色版的RGB影像，即可提供不透明度資訊。 此外，整體不透明度可隨以下專案變化： `opacity=` 指令(適用於RGB和RGBA影像)。

壁邊界也支援RGBA影像，主要是為了支援壓鑄模切削邊界。

此 [!DNL vnw] 定義視窗涵蓋範圍的檔案可包含不透明度通道。 它由轉譯器與可重複紋理的Alpha色版結合，並且 `opacity=` 其價值在於提供各種不透明效果，適用於透明和半透明視窗處理。
