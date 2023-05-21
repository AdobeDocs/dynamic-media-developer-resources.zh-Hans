---
title: 根路徑
description: 來源資料根路徑。 文字字串值。 此影像目錄參照之所有暈映、紋理、影像和ICC資料檔的根資料夾絕對路徑或相對路徑區段。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# 根路徑{#rootpath}

來源資料根路徑。 文字字串值。 此影像目錄參照之所有暈映、紋理、影像和ICC資料檔的根資料夾絕對路徑或相對路徑區段。

## 屬性 {#section-5ff1cf592dd24dfc8cfa470c753ab828}

文字字串。 必須為空白，為相對於影像演算伺服器組態設定的有效路徑區段 `ir.resourceRootPaths`或有效的絕對檔案路徑。 不應包含前置和結尾路徑元素分隔字元。

## 默认 {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

繼承自 `default::RootPath` 若未定義。 如果已定義但為空，則不會對來源檔案根路徑產生任何影響。

## 另请参阅 {#section-92012cc1ce32448ea977e7e0484857e2}

[catalog：：Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) ， [catalog：：AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969)， `ir.resourceRootPaths`
