---
title: 巢狀影像演算請求
description: 對於進階應用程式，可以將轉譯作業的結果當做材質影像使用，就像從「影像伺服」取得的影像一樣。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# 巢狀影像演算請求{#nested-image-rendering-requests}

對於進階應用程式，可以將轉譯作業的結果當做材質影像使用，就像從「影像伺服」取得的影像一樣。

轉譯請求可透過在 `src=` 命令，如下所示：

` …&src=ir{ *[!DNL renderRequest]*}&…`

此 `ir` Token區分大小寫。

巢狀請求不得包含影像演算根路徑(通常是 `http:// *[!DNL server]*/ir/render/'`)，但可能包含預先處理規則Token。

在巢狀請求中指定時(在請求url中或在 `catalog::Modifier` 或 `catalog::PostModifier`)：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

同樣被忽略的是 `attribute::MaxPix` 和 `attribute::DefaultPix` 套用至巢狀轉譯器請求的材質目錄的。

可選擇快取巢狀IR要求的影像結果，方法是包含 `cache=on`. 依預設，會停用中繼資料的快取。 只有在合理時段內不同的請求中重複使用中間影像時，才應啟用快取。 標準伺服器端快取管理適用。 資料會以無損格式快取。
