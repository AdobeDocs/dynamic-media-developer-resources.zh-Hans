---
title: 限制
description: 巢狀和內嵌有一些限制。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# 限制{#restrictions}

巢狀和內嵌有一些限制。

為了提供良好的伺服器效能，巢狀要求傳回的影像解析度應適當地符合套用材質之物件的紋理解析度。

本機快取外部影像。 只有在本機快取專案過時後（根據expires HTTP標頭），才會偵測到這類影像的任何變更。
