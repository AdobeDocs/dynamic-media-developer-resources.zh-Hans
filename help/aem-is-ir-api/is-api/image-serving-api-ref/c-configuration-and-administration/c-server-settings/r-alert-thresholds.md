---
description: 使用这些服务器设置配置警报阈值。
solution: Experience Manager
title: 警报阈值
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# 警报阈值{#alert-thresholds}

使用这些服务器设置配置警报阈值。

## AS：： monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS：： monitorAlertGenerator.maxAverageResponseTime -Response Time {#section-35111039ac6c4a63ba23fc2c828ab726}

当采样间隔内处理请求的平均时间超过此处设置的阈值时，将发出响应时间警报。 以毫秒为单位表示；整数0或更大。 根据操作的复杂性，典型值为100到1000毫秒。

>[!NOTE]
>
>此警报不考虑导致4xx或5xx响应状态的请求。

## AS：：monitorAlertGenerator.maxErrorRate — 错误响应率ThresholdAS：：monitorAlertGenerator.maxErrorRate — 错误响应率 {#section-76ba77fd3102419395e0f86719a1f3ec}

当取样间隔内HTTP错误响应与总响应的比率超过指定的阈值时，将发出错误警报。

介于0.0和1.0之间的实际值。通常设置为介于0.005和0.1之间。设置为1可禁用错误警报。

## AS：：monitorAlertGenerator.minRequestRate — 低流量阈值 {#section-8dfb89ed138640fd86f5ce1dae2a533e}

在当前采样间隔内每秒接收的平均请求数低于此阈值时，将发送最小流量警报。 将此值设置为0可禁用警报。 以每秒请求数表示。 大于或等于0的实值。

## AS：：monitorAlertGenerator.minFreeHeapSpace -Free栈空间阈值 {#section-ce6705045f6842769030ccb1894594cc}

指定最小可用Java栈空间。 当可用栈空间低于此阈值时，在Java垃圾回收循环后立即发送优先级警报。 建议50 MB以安全运行[!DNL Platform Server]。 将可用栈空间保持在此值之上可减少垃圾回收周期的频率，从而改善整体服务器性能。 以字节为单位的整数值，0或更大。

## AS：：monitorAlertGenerator.maxOverlap — 最大并发请求数 {#section-ddc6925bff944758ab19bcc9cf3f2589}

当在平均间隔期间并发处理的平均请求数超过此阈值时，将触发重叠警报。 重叠程度高可能表示存在服务器过载情况。

整数值1或更大。 典型范围为20到50，具体取决于缓存命中率和请求复杂性。

## AS：：monitorAlertGenerator.lockedThreshold — 锁定的请求阈值 {#section-012a1c9937d445708380339279c62d80}

指定请求在被视为锁定或挂起之前必须处于挂起状态的秒数。 如果在平均间隔结束时，至少有一个请求已挂起超过指定时间段，则会发出锁定请求警报。 正整数值（毫秒）。

要解决复杂的渲染请求和涉及从外部HTTP服务器获取数据的请求，建议将此值设置为至少30秒（除非此警报将检测到此类条件）。
