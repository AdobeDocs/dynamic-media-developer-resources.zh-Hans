---
description: 您可以在伺服器上線時，在覆寫檔案之前使用req=release命令來取代或刪除暈映檔案。
solution: Experience Manager
title: 刪除或取代來源資料檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# 刪除或取代來源資料檔案{#deleting-or-replacing-source-data-files}

您可以在伺服器上線時，在覆寫檔案之前使用req=release命令來取代或刪除暈映檔案。

>[!NOTE]
>
>當轉譯器伺服器存取資料檔時，不能取代或刪除資料檔。

請記住，刪除或取代來源資料檔案只會讓轉譯器伺服器關閉檔案，直到存取該暈映的下一個請求為止。 如果檔案使用量很大，則可能需要多次重試。

必須停止轉譯伺服器才能取代其他資料檔案。

[!DNL Platform Server] 當材料檔案或暈映被取代時，快取專案會自動失效。 取代ICC設定檔不會使快取失效。

為了避免取代檔案的複雜性，建議為取代檔案指定新名稱，並更新對應的目錄專案。 這允許在伺服器上線時取代任何資料檔案，並導致伺服器快取專案自動過時，不需要額外的介入。 此方法可用於影像目錄管理的所有資料檔案。
