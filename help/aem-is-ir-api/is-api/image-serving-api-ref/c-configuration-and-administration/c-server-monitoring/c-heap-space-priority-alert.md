---
description: 当可用Java堆空间在紧随Java垃圾收集周期后的指定阈值以下时，将发送优先级警报。
seo-description: 当可用Java堆空间在紧随Java垃圾收集周期后的指定阈值以下时，将发送优先级警报。
seo-title: 堆空间优先级警报
solution: Experience Manager
title: 堆空间优先级警报
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# 堆空间优先级警报{#heap-space-priority-alert}

当可用Java堆空间在紧随Java垃圾收集周期后的指定阈值以下时，将发送优先级警报。

应通过增加Java堆空间来解决重复的警报。 在用`AS::monitorAlertGenerator.heapSpaceResetInterval`指定的延迟期过期之前，随后出现此情况不会导致电子邮件警报。
