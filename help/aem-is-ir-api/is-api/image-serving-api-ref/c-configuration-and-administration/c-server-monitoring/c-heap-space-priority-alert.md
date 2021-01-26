---
description: 当可用Java堆空间在紧随Java垃圾收集周期之后低于指定阈值时，将发送优先级警报。
seo-description: 当可用Java堆空间在紧随Java垃圾收集周期之后低于指定阈值时，将发送优先级警报。
seo-title: 堆空间优先级警报
solution: Experience Manager
title: 堆空间优先级警报
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# 堆空间优先级警报{#heap-space-priority-alert}

当可用Java堆空间在紧随Java垃圾收集周期之后低于指定阈值时，将发送优先级警报。

应通过增加Java堆空间来解决重复的警报。 在用`AS::monitorAlertGenerator.heapSpaceResetInterval`指定的延迟期已过之前，此条件的后续出现不会导致电子邮件警报。
