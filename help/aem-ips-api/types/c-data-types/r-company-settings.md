---
description: 公司特定的組態設定。
solution: Experience Manager
title: 公司設定
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 2%

---

# [!DNL CompanySettings]{#companysettings}

公司特定的組態設定。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| overwriteMode | `xsd:string` | 決定是否以相同的基本影像名稱和副檔名覆寫目前資料夾中的影像。 |
| retainPublishState | `xsd:boolean` | 指定上載至IPS的取代影像是否應保留現有的「準備發佈」設定，或是否應該依照上載的指定。 |
| defaultSourceProfile | `types:Asset` | 指定增加CMYK影像檔案時，作為「使用預設色彩行為」的一部分自動套用的預設來源色彩設定檔(Coated FOGRA27 (ISO 126472：2004))。 |
| defaultDisplayprofile | `types:Asset` | 指定預設內部色彩設定檔(U.S. Web Coated (SWOP) v2)在增加CMYK影像檔案時，會自動套用為「使用預設色彩行為」的一部分。 |
| iptcExifMappingXslt | `types:Asset` | 將IPTC和EXIF影像標頭資料擷取到IPS需要從內部欄位名稱轉換為公司使用者定義的欄位名稱。 決定上傳影像的XSL轉譯表格（預設值為「不擷取任何IPTC或EXIF欄位」）。 |
| xmpMappingXslt | `types:Asset` | 將XMP影像標題資料擷取至IPS時，需要從內部欄位名稱轉換為公司使用者定義的欄位名稱。 決定已上傳影像的XSL轉譯表格(預設值為「不擷取任何XMP欄位」)。 |
| diskSpaceWarningMin | `xsd:int` | 發出警告之前的最小影像目錄可用磁碟空間。 |
| emailTrashCleanupWarning | `xsd:boolean` | 決定是否要在自動刪除置入垃圾桶中的專案之前傳送電子郵件。 |
| Javascriptuploadenabled | `types:Asset` | 決定是否上傳JavaScript檔案。 這是潛在的安全性風險，因此請謹慎使用此選項。 |
