---
description: 當可用的Java棧積空間低於指定的臨界值時，優先順序警報會在Java垃圾收集循環後立即傳送。
solution: Experience Manager
title: 棧積空間優先順序警報
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# 棧積空間優先順序警報{#heap-space-priority-alert}

當可用的Java棧積空間低於指定的臨界值時，優先順序警報會在Java垃圾收集循環後立即傳送。

應增加Java棧積空間來解決重複的警報。 後續發生此狀況時，直到指定的延遲期間後，才會產生電子郵件警示。 `AS::monitorAlertGenerator.heapSpaceResetInterval` 已過期。
