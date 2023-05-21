---
description: 影像遮色片。 要求遮罩（Alpha色版）資料。
solution: Experience Manager
title: 遮色片
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 13%

---

# 遮色片{#mask}

影像遮色片。 要求遮罩（Alpha色版）資料。

`req=mask`

支援與相同的命令 `req=img`. 伺服器會以相同的方式處理它，但不會傳回RGB或RGBA資料，而是捨棄顏色資訊並只傳回遮色片（Alpha色版）資料。 回覆資料格式和回應MIME型別由以下專案決定 `fmt=`.

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.
