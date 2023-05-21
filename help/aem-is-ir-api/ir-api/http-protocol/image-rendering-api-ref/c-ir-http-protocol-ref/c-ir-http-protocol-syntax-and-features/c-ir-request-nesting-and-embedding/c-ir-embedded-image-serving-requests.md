---
title: 內嵌影像伺服器要求
description: 影像伺服器(IS)要求可作為材質影像使用。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# 內嵌影像伺服器要求{#embedded-image-server-requests}

影像伺服器(IS)要求可作為材質影像使用。

在中指定請求 `src=` 命令，如下所示：

` …&src=is( *[!DNL imageServingRequest]*)&…`

此 `is` Token區分大小寫。

巢狀請求不得包含影像伺服根路徑(通常是 [!DNL http:// *[!DNL server]*/is/image/"])，但可能包含預先處理規則Token。

在巢狀請求中指定下列IS命令時(在請求URL中或在 `catalog::Modifier` 或 `catalog::PostModifier`)：

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

同樣被忽略的是 `attribute::MaxPix` 和 `attribute::DefaultPix` 套用至內嵌IS要求的影像目錄的ID。

如果巢狀請求的結果影像包含遮色片(Alpha)資料，則一律會傳遞至材質。 使用純色背景影像圖層來避免不想要的Alpha。

可選擇快取內嵌IS要求的影像結果，方法是包含 `cache=on`. 依預設，會停用中繼資料的快取。 只有在合理時段內不同的請求中重複使用中間影像時，才應啟用快取。 標準伺服器端快取管理適用。 資料會以無損格式快取。
