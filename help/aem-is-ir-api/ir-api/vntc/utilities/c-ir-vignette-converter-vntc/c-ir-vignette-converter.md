---
description: 暈映轉換程式(vntc)是命令列公用程式，用來準備使用影像製作所建立的內容，以使用影像演算部署。
solution: Experience Manager
title: 暈映轉換工具
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 暈映轉換工具{#vignette-converter}

暈映轉換程式(vntc)是命令列公用程式，用來準備使用影像製作所建立的內容，以使用影像演算部署。

[!DNL vntc] 位於[！DNL *[!DNL install_root]*\ImageServing\bin]。 它有下列功能：

* 將主要暈映轉換為單一解析度、多解析度或金字塔生產暈映(請參閱 [暈映縮放](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585))。
* 產生生產封包和視窗涵蓋樣式檔案(請參閱 `-resolution` 和 `-jpegquality`)。

* 可以產生不同版本的暈映、檔案櫃和視窗覆蓋樣式檔案，以搭配較舊版本的影像演算使用。
* 從完整解析度或縮圖的暈映擷取檢視影像(請參閱 `-thumbwidth` 和 `-image`)。
* 從來源檔案擷取相關屬性(請參閱 `-info`)並傳送至 `stdout` 或選用的記錄檔(請參閱 `-log`)。

當使用 [!DNL vntc] 是選用專案，強烈建議使用它以獲得最佳伺服器效能。 [!DNL vntc] 此外，還實施廣泛的錯誤檢查，並可防止嚴重伺服器問題（包括當機）。

產生生產暈映時，輸出暈映的畫素寬度（如果是金字塔或多解析度暈映，則為0）會附加至產生的輸出暈映檔案的名稱中。 處理封包樣式檔案時，輸出解析度會附加至輸出檔案名稱。 所有輸出檔案（包括選用的縮圖、影像和記錄檔）以及生產暈映或封包樣式檔案都放在相同的目錄中，其中 *[!DNL sourceFile]* 位置(除非 `-destPath` （已指定）。

[!DNL vntc] 預設會將其自身限製為最多3GB的記憶體。 當Vntc達到此限制時，它將停止處理並將產生錯誤。 此限制可使用以下變更： `-maxmem`.

>[!NOTE]
>
>影像製作中的暈映更新工具也可用來準備用於影像演算的暈映。 同樣地，「內容製作工具」也能產生封包樣式檔案，以與「影像演算」搭配使用。 使用 [!DNL vntc] 如果處理作業要自動化。 影像製作中的工具包括圖形化使用者介面，因此通常更易於以互動方式使用。

## 另请参阅 {#section-3c756bf17b634543904fdd928adeafb2}

影像製作檔案
