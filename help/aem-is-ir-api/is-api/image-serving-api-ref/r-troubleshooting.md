---
description: 本節包含「影像伺服」偶爾發生問題的解決方案。
solution: Experience Manager
title: 疑难解答
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b80d3c9a-a0c4-4944-9f91-e791a072cd5f
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# 疑难解答{#troubleshooting}

本節包含「影像伺服」偶爾發生問題的解決方案。

**常规**

ImageServer現在會保留在升級安裝期間變更的所有檔案的安裝記錄檔和備份資料夾。 此檔案和資料夾可在「影像伺服」安裝目錄的根目錄下找到。

**啟動影像伺服器時，啟動指令碼會停頓並顯示「啟動擱置」訊息（僅限LINUX）**

這可能表示「影像伺服」授權有問題，例如遺失授權檔案或暫存授權過期。 有效的授權檔案必須位於 [!DNL /usr/local/scene7/licenses].

**Image Server停止或當機，且Image Server記錄檔指出檔案中的空間不足或「資源暫時無法使用」 [!DNL IgcVirtualMemory.cpp]&quot;**

此錯誤訊息的原因是Image Server無法配置其設定為使用的記憶體數量。

* 檢查中的實體記憶體設定 [!DNL ImageServerRegistry.xml]. 如果其他耗用大量記憶體的應用程式在同一系統上執行，則不應超過50%。 預設值為20%。
* 請確定伺服器上的交換空間至少是實體RAM大小的兩倍。 交換空間設定過低會導致此問題。

**快取資料夾使用的實際磁碟空間超過 ` *[!DNL cache.maxSize]*`設定於[!DNL PlatformServer.conf]**

這並不表示有問題。 檔案系統開銷不包含在中 [!DNL Platform Server]的磁碟快取設定。 系統報告的總量可能會大幅超過設定。 建議保留兩倍的磁碟空間 ` *[!DNL cache.maxSize]*`.

**is-docs範例中的損壞影像**

如果影像伺服器未執行，就會發生這種情況。 如果目錄根路徑或影像根路徑已從安裝預設值變更，但範例影像和目錄尚未移至新位置，也會發生這種情況。 檢查組態檔中的影像伺服器根路徑值。 如有必要，請將包含範例影像的示範資料夾移至目前的影像根目錄，然後移動 [!DNL sample*.*] 至目前目錄根目錄。

這些範例也假設中的某些設定 [!DNL default.ini] 是標準的（例如不得啟用模糊化或鎖定）。

**長時間運作後遺漏太多快取**

視伺服器使用狀況而定，效能可能會透過提高伺服器使用狀況來改善 [!DNL Platform Server] 磁碟快取大小（如果磁碟空間可用）。 您可以手動編輯組態檔來變更設定。 請參閱檔案。

**記錄檔佔用太多磁碟空間**

影像伺服器和 [!DNL Platform Server] 每天啟動新的記錄檔。 依預設，這些檔案會放在[！DNL *[!DNL install_root]*/ImageServing/logs]。 記錄檔大小、保留的記錄數以及可設定的記錄內容。 請參閱檔案。

**如果您的伺服器已安裝防毒軟體**

建議您關閉「影像伺服」目錄的掃描。 否則，掃描大量讀取/寫入目錄（例如快取、影像、字型、設定檔和目錄目錄）將會造成問題。

**Digimarc造成縮放影像的效能問題**

請勿在已縮放的影像上使用Digimarc。 無法接受此效能。 如有必要，請為影像建立個別目錄，以用於縮放和停用此目錄的Digimarc。
