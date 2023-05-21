---
description: 本主題說明vntc使用語法。
solution: Experience Manager
title: 使用
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%

---

# 使用{#usage}

本主題說明vntc使用語法。

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* 是要處理的檔案的路徑和名稱。 可以是相對於目前工作目錄的路徑或絕對路徑。 必須是有效的暈映、封包樣式或視窗涵蓋樣式檔案，並具有下列尾碼之一： [!DNL .vnt]， [!DNL .vnc]，或 [!DNL .vnw]. 必需.

*[!DNL destFile]* 是輸出暈映檔案的路徑和名稱。 如果未指定，則會將輸出檔案放置在指定的資料夾中 `-destpath`. 在此案例中，檔案名稱會自動從輸入檔案名稱和大小尾碼產生，以指定的字串分隔 `-separator`. 對於暈映，大小字尾是單解析度輸出暈映的畫素寬度、多解析度輸出暈映的第一個檢視的寬度，或是金字塔暈映的「0」。 對於封包樣式檔案，輸出解析度會用作檔案字尾。 *[!DNL destFile]* 忽略於 `-info` 已指定。
