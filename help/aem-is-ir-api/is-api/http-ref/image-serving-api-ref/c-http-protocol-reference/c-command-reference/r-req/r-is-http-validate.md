---
description: 要求驗證。
solution: Experience Manager
title: 确认
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88424371-45a0-43bb-af49-2e8568b7b44c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 4%

---

# 确认{#validate}

要求驗證。

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>唯一請求識別碼。 </p></td> 
 </tr> 
</table>

剖析請求字串，如下所示 `req=img` 已指定，但未取代變數及評估參照的物件（影像、ICC設定檔、字型等）。 剖析失敗時會傳回標準錯誤回應，否則會傳回下列屬性：

`request.isValid=1`

無法快取HTTP回應。

支援JSONP回應格式的請求可讓您使用擴充語法來指定JS回呼處理常式的名稱。 `req=` 引數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中呈現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 可选. 默认值为 `s7jsonResponse`.
