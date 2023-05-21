---
title: 要求預先處理
description: 「影像演算」會根據規則運算式比對和替代規則，提供簡單的要求前置處理器。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
source-git-commit: 20f4922402bd31c71ae650a01597b574220809fa
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# 要求預先處理{#request-pre-processing}

「影像演算」會根據規則運算式比對和替代規則，提供簡單的要求前置處理器。

規則（規則集）集合可附加至每個材料目錄，包括預設目錄。 規則是以XML格式檔案指定的。

請求預先處理規則可在影像演算剖析器處理請求之前，修改請求的路徑和查詢部分。 此原則包括操控路徑、新增命令、變更命令值，以及套用範本或巨集。 規則也可用來設定和覆寫某些功能，這些功能通常僅由目錄屬性控制，例如設定預設回覆影像大小或將HTTP服務限製為特定使用者端IP位址。

要求預先處理規則適用於各種應用程式，其中一些如下所列：

* 實作 *虛擬路徑* 機制，允許將請求路徑重新對應到檔案、FTP和HTTP路徑。
* 不允許使用耗用CPU的命令來防止伺服器濫用。
* 根據請求路徑或影像名稱控制影像品質設定(例如JPEG品質或銳利化)。

有關建立、使用和管理規則集的詳細資訊，請參閱「規則集參考」。

另請參閱規則集參考、屬性：：RuleSetFile
