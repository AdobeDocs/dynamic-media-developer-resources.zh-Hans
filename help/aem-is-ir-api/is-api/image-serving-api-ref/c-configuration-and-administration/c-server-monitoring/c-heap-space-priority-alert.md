---
description: 当可用Java栈空间在紧接Java垃圾收集循环之后低于指定的阈值时，将发送优先级警报。
solution: Experience Manager
title: 栈空间优先级警报
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# 栈空间优先级警报{#heap-space-priority-alert}

当可用Java栈空间在紧接Java垃圾收集循环之后低于指定的阈值时，将发送优先级警报。

应通过增加Java栈空间来解决重复的警报。 在通过`AS::monitorAlertGenerator.heapSpaceResetInterval`指定的延迟时段到期之前，此情况的后续发生不会导致电子邮件警报。
