---
description: 当可用Java堆空间低于紧随Java垃圾收集循环的指定阈值时，将发送优先级警报。
seo-description: 当可用Java堆空间低于紧随Java垃圾收集循环的指定阈值时，将发送优先级警报。
seo-title: 堆空间优先级警报
solution: Experience Manager
title: 堆空间优先级警报
topic: Scene7 Image Serving - Image Rendering API
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 堆空间优先级警报{#heap-space-priority-alert}

当可用Java堆空间低于紧随Java垃圾收集循环的指定阈值时，将发送优先级警报。

应通过增加Java堆空间来解决重复的警报。 此条件的后续出现不会导致电子邮件警报，直到指定的延迟期 `AS::monitorAlertGenerator.heapSpaceResetInterval` 已到期。
