---
description: 回應CDN失效請求中一個URL的詳細訊息。
solution: Experience Manager
title: Operationfault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 12%

---

# [!DNL OperationFault]{#operationfault}

回應CDN失效請求中一個URL的詳細訊息。

**支援開始時間**

4.5.0，修補程式2011-02

## 参数 {#section-cf4b0c923cef4c14869319af73ace58b}

| ** 名称** | ** 类型** | ** 说明** |
|---|---|---|
| 代码 | `xsd:int` | CDN提供的錯誤代碼 |
| 原因 | `xsd:string` | CDN提供的錯誤訊息 |
