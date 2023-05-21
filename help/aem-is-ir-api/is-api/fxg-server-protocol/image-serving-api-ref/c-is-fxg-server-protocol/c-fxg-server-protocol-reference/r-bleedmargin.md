---
description: 設定出血邊界。 設定PDF檔案中設定的出血邊界。
solution: Experience Manager
title: 出血邊界
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# 出血邊界{#bleedmargin}

設定出血邊界。 設定PDF檔案中設定的出血邊界。

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` 點數

根據預設 `bleedMargin` 設為所定義檔案的完整大小 `viewWidth` 和 `viewHeight`. 此 *[!DNL left]*， *[!DNL bottom]*、和 *[!DNL right]* 值會預設為 *[!DNL top]* 值（若未指定）。
