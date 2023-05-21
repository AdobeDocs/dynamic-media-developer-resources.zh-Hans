---
description: 影像已存在。
solution: Experience Manager
title: 存在
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# 存在{#exists}

影像已存在。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 唯一請求識別碼

傳回名為的單一屬性 `catalogRecord.exists`. 如果影像或預設目錄中存在指定的目錄專案，則屬性值會設為「1」，否則會設為「0」。 `req=exists` 針對以下專案的請求： `/is/content` 上下文將指示靜態內容目錄中是否存在指定記錄。

請求字串中的其他命令會被忽略。 HTTP 响应是可缓存的，且 TTL 基于 `attribute::NonImgExpiration`.

支援JSONP回應格式的請求可讓您使用擴充語法來指定JS回呼處理常式的名稱。 `req=` 引數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中呈現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 可选. 默认值为 `s7jsonResponse`.
