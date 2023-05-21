---
description: 影像（預設）。 要求標準影像資料。
solution: Experience Manager
title: img
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5338358e-755b-41d6-a941-8754d0deb9aa
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 21%

---

# img{#img}

影像（預設）。 要求標準影像資料。

`req=img`

回覆資料格式和回應MIME型別由以下專案決定 `fmt=`. `req=img` 是預設要求型別，不需要明確指定。 HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

其他要求命令會依檔案說明套用。
