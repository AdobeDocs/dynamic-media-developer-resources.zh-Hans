---
description: 如果要求成功完成，且要求未包含req=命令，或req=img或req=tmb，則會傳回影像資料。
solution: Experience Manager
title: 图像
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 1%

---

# 图像{#images}

如果要求成功完成，且要求未包含req=命令，或req=img或req=tmb，則會傳回影像資料。

HTTP回應MIME型別由以下專案決定 `fmt=`，或，如果 `fmt=` 未指定，它是 `<image/jpeg>`.

如果要求方法為無條件，則HTTP回應狀態為「200 OK」 `GET` 或 `HEAD`.

伺服器可能會以「304」狀態回覆（未修改），並且不會傳回任何影像資料來回應條件 `GET` 請求(包括有效的 `If-Modified-Since` 或 `If-None-Match` 標頭)。
