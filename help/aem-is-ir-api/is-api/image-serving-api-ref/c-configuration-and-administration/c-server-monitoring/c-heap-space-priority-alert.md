---
description: 当可用Java堆空间在Java垃圾收集周期之后紧接在指定的阈值之下时，将发送优先级警报。
solution: Experience Manager
title: 堆空间优先级警报
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# 堆空间优先级警报{#heap-space-priority-alert}

当可用Java堆空间在Java垃圾收集周期之后紧接在指定的阈值之下时，将发送优先级警报。

应通过增加Java堆空间来解决重复的警报。 在通过`AS::monitorAlertGenerator.heapSpaceResetInterval`指定的延迟期到期之前，后续出现此条件不会生成电子邮件警报。
