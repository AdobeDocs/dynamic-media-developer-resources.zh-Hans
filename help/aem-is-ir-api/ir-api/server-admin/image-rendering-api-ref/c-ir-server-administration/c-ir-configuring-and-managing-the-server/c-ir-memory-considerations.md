---
description: 影像演算使用的記憶體量可能會有很大的差異，而且很大程度上取決於實際的伺服器負載和使用情況（例如，很少有和許多不同的暈映、暈映的大小和複雜度等等）。
solution: Experience Manager
title: 記憶體考量事項
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# 記憶體考量事項{#memory-considerations}

影像演算使用的記憶體量可能會有很大的差異，而且很大程度上取決於實際的伺服器負載和使用情況（例如，很少有和許多不同的暈映、暈映的大小和複雜度等等）。

為獲得最佳效能，應避免記憶體分頁（交換）。

影像演算共用影像伺服器的記憶體管理。 使用影像演算時，應配置額外的記憶體。 30%到50%的實體記憶體可能比較合理。

如需有關如何變更影像伺服器記憶體配置的資訊，請參閱「影像伺服」檔案(ImageServer：：PhysicalMemory)。
