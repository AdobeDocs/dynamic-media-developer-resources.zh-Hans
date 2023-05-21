---
description: 在URL或catalog Modifier命令序列中，圖層定義序列以layer=命令開頭，以另一個layer=命令、effect=命令或URL結尾結束。
solution: Experience Manager
title: 指定圖層
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# 指定圖層{#specifying-layers}

在URL或catalog：：Modifier命令序列中，圖層定義序列以layer=命令開頭，以另一個layer=命令、effect=命令或URL結尾結束。

圖層定義序列中的所有指令都與圖層相關聯。

此 `layer=` command指定圖層編號，它必須是大於或等於0的整數。 具有相同圖層編號的圖層定義序列中的所有指令都會套用至相同的圖層。 如果同一命令發生多次，則最後一個例項將優先。
