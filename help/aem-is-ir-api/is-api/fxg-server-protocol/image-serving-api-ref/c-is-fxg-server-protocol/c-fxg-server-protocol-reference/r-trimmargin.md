---
description: 設定裁剪邊界。 設定PDF檔案中設定的裁剪邊界。
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# trimMargin{#trimmargin}

設定裁剪邊界。 設定PDF檔案中設定的裁剪邊界。

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` 點數

根據預設 `trimMargin` 設為所定義檔案的完整大小 `viewWidth` 和 `viewHeight`. 此 *[!DNL left]*， *[!DNL bottom]*、和 *[!DNL right]* 值會預設為 *[!DNL top]* 值（若未指定）。
