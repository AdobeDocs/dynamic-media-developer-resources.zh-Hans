---
description: 預設目錄為所有影像目錄的所有目錄屬性提供預設值。
solution: Experience Manager
title: 預設目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# 預設目錄{#default-catalog}

預設目錄為所有影像目錄的所有目錄屬性提供預設值。

如果特定影像目錄中找不到特定屬性，則伺服器會改用預設目錄中的對應值。 同樣地，預設目錄可用於為特定目錄資料記錄（影像、巨集定義、字型和ICC設定檔）提供預設值。 如果在特定影像目錄中找不到特定資料記錄，則伺服器會嘗試在預設目錄中尋找該記錄。 如此可讓影像目錄稀疏填入，並簡化全域屬性和資料（例如共用範本、巨集、字型等）的管理。

此外，預設目錄會在作業中不包含特定影像目錄時，提供所有屬性和資料記錄（巨集、字型、ICC設定檔、要求前置處理規則）。

為了正確運作 [!DNL Platform Server] 預設目錄的目錄屬性檔案必須命名為 [!DNL default.ini]，且必須一律存在於目錄資料夾中，且必須填入所有必要的屬性，惟不包括 `attribute::RootId` 和各種目錄資料檔案的參照，這些檔案都是選用的。

>[!NOTE]
>
>所有目錄屬性檔案，但不包括 [!DNL default.ini] 必須包含唯一 `attribute::RootId` 值。 `attribute::RootId` 在 [!DNL default.ini] 必須為空白。
