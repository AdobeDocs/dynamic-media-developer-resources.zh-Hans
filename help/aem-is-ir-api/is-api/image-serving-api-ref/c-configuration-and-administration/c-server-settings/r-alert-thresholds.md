---
description: 使用这些服务器设置配置警报阈值。
solution: Experience Manager
title: 警报阈值
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# 警报阈值{#alert-thresholds}

使用这些服务器设置配置警报阈值。

## 作为：monitorAlertGenerator.maxAverageResponseTime — 响应时间阈值AS:monitorAlertGenerator.maxAverageResponseTime — 响应时间 {#section-35111039ac6c4a63ba23fc2c828ab726}

当在采样间隔期间处理请求的平均时间超过此处设置的阈值时，发出响应时间警报。 以毫秒表示；整数0或更大。 典型值介于100到1000毫秒之间，具体取决于操作的复杂性。

>[!NOTE]
>
>此警报不考虑导致4xx或5xx响应状态的请求。

## AS::monitorAlertGenerator.maxErrorRate — 错误响应率阈值AS::monitorAlertGenerator.maxErrorRate — 错误响应率 {#section-76ba77fd3102419395e0f86719a1f3ec}

当采样间隔期间HTTP错误响应与总响应的比率超过指定的阈值时，将发出错误警报。

0.0到1.0之间的实际值。通常设置为0.005到0.1之间。设置为1可禁用错误警报。

## AS::monitorAlertGenerator.minRequestRate — 低流量阈值 {#section-8dfb89ed138640fd86f5ce1dae2a533e}

当当前采样间隔内每秒接收的请求数平均数低于此阈值时，将发送最小流量警报。 将此值设置为0，以禁用警报。 以每秒请求数表示。 实际值0或更大。

## AS::monitorAlertGenerator.minFreeHeapSpace — 可用堆空间阈值 {#section-ce6705045f6842769030ccb1894594cc}

指定最小可用Java堆空间。 当可用堆空间低于此阈值时，将在Java垃圾收集周期后立即发送优先级警报。 建议50 MB以安全运行平台服务器。 将可用堆空间保持在此值以上会减少垃圾收集周期的频率，这可能会提高整体服务器性能。 整数值（以字节为单位，0或更大）。

## AS::monitorAlertGenerator.maxOverlap — 并发请求的最大数量 {#section-ddc6925bff944758ab19bcc9cf3f2589}

在平均间隔期间同时处理的平均请求数超过此阈值时，将触发重叠警报。 高重叠可能表示服务器过载情况。

整数值1或更大。 根据缓存点击率和请求复杂度，典型值范围为20到50。

## AS::monitorAlertGenerator.lockedThreshold — 锁定请求阈值 {#section-012a1c9937d445708380339279c62d80}

指定请求在被视为锁定或挂起之前必须处于挂起状态的秒数。 如果在平均间隔结束时至少有一个请求处于挂起状态的时间超过指定时间段，则发出锁定请求警报。 正整数值（毫秒）。

要考虑到涉及从外部HTTP服务器获取数据的复杂呈现请求和请求，建议将此值至少设置为30秒（除非此警报会检测到此情况）。
