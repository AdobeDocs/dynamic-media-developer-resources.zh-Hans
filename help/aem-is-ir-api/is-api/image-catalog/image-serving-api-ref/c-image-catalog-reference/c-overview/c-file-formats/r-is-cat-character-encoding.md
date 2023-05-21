---
description: 「影像伺服」支援採用ISO-8859-1和UTF-8編碼的影像目錄。
solution: Experience Manager
title: 字元編碼
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# 字元編碼{#character-encoding}

「影像伺服」支援採用ISO-8859-1和UTF-8編碼的影像目錄。

位元組順序標籤(BOM)可用來指定每個檔案的編碼。 對於UTF-8，BOM是位元組順序 `EF BB BF`. 在每個影像目錄檔案的開頭偵測到此字元序列時，會採用UTF-8編碼。 任何其他位元組序列都會將檔案解譯為編碼為ISO-8859-1標準。

許多當代應用程式在針對UTF-8進行配置時，會自動插入BOM。
