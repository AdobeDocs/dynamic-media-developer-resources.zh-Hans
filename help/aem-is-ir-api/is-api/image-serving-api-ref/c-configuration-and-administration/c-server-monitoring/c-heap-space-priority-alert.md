---
description: 当可用Java堆空间在紧随Java垃圾收集周期后的指定阈值以下时，将发送优先级警报。
solution: Experience Manager
title: 堆空间优先级警报
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# 堆空间优先级警报{#heap-space-priority-alert}

当可用Java堆空间在紧随Java垃圾收集周期后的指定阈值以下时，将发送优先级警报。

应通过增加Java堆空间来解决重复的警报。 在用`AS::monitorAlertGenerator.heapSpaceResetInterval`指定的延迟期过期之前，随后出现此情况不会导致电子邮件警报。
