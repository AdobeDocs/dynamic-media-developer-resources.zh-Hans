---
title: 外部影像來源
description: 「影像伺服」支援對外國HTTP和FTP伺服器上的來源影像的存取。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# 外部影像來源{#foreign-image-sources}

「影像伺服」支援對外國HTTP和FTP伺服器上的來源影像的存取。

若要為指定外部URL `src=` 或 `mask=` 命令；只要使用大括弧分隔整個內嵌URL即可：

` …&src={ *[!DNL foreignUrl]*}&…`

完整絕對URL (若 `attribute::AllowDirectUrls` 「 」和「 URL 」相對於 `attribute::RootUrl` 允許。 如果內嵌絕對URL且屬性為： `AllowDirectUrls` 為0，或如果已指定相對URL，且 `attribute::RootUrl` 空白。

伺服器會根據HTTP回應隨附的快取標頭快取外部影像。
