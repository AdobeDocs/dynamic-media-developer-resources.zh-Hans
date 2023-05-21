---
description: 雖然新增資料檔案簡單明瞭，但在取代伺服器主動使用的現有資料檔案時，必須特別小心。 建議不要簡單地取代此類檔案，而是為取代檔案提供一個新名稱（例如，在檔案名稱后面附加一個版本字尾）。 新檔案上線後，即可刪除舊版本。
solution: Experience Manager
title: 刪除或取代資料檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 刪除或取代資料檔案{#deleting-or-replacing-data-files}

雖然新增資料檔案簡單明瞭，但在取代伺服器主動使用的現有資料檔案時，必須特別小心。 建議不要簡單地取代此類檔案，而是為取代檔案提供一個新名稱（例如，在檔案名稱后面附加一個版本字尾）。 新檔案上線後，即可刪除舊版本。

>[!NOTE]
>
>「影像伺服」使用中時，絕不可取代或刪除資料檔案。 否則可能會發生錯誤或甚至伺服器當機。

在所有情況下，請記住 [!DNL Platform Server] 快取和使用者端快取專案必須過時後，使用者端才能看到更新的資料。 特定的快取專案可使用以下專案立即更新： `cache=validate` 命令。

快取管理員不會直接追蹤字型檔案和ICC設定檔的變更。 如果修改這類資源而不變更其ID，伺服器快取將無法得知變更，並且 `cache=validate` 不會導致快取專案更新。 `cache=update` 可用來強制重新產生這類快取專案。

為了避免取代檔案的複雜性，建議為取代檔案指定新名稱，並更新對應的目錄專案。 這將允許在伺服器上線時取代任何資料檔案，並導致伺服器快取專案立即過時，不需要額外的介入。 此方法可用於ICC設定檔、字型和影像目錄管理的所有影像。
