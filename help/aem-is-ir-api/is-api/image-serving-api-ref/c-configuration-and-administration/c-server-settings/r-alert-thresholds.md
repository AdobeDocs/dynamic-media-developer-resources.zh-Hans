---
description: 使用这些服务器设置配置警报阈值。
seo-description: 使用这些服务器设置配置警报阈值。
seo-title: 警报阈值
solution: Experience Manager
title: 警报阈值
uuid: 032cb396-1a03-4ba9-82d6-ed2cb06e8cf2
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---


# 警报阈值{#alert-thresholds}

使用这些服务器设置配置警报阈值。

## AS:monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS:monitorAlertGenerator.maxAverageResponseTime -Response Time {#section-35111039ac6c4a63ba23fc2c828ab726}

当在采样间隔期间处理请求的平均时间超过此处设置的阈值时，发出响应时间警报。 以毫秒表示；整数0或更大。 典型值介于100和1000毫秒之间，具体取决于操作的复杂性。

>[!NOTE]
>
>此警报不考虑导致4xx或5xx响应状态的请求。

## AS::monitorAlertGenerator.maxErrorRate — 错误响应速率ThresholdAS::monitorAlertGenerator.maxErrorRate — 错误响应速率{#section-76ba77fd3102419395e0f86719a1f3ec}

当在采样间隔期间HTTP错误响应与总响应的比率超过指定阈值时发出错误警报。

0.0到1.0之间的实数值。通常设置为0.005到0.1之间。设置为1可禁用错误警报。

## AS::monitorAlertGenerator.minRequestRate — 低流量阈值{#section-8dfb89ed138640fd86f5ce1dae2a533e}

当在当前采样间隔期间每秒接收的平均请求数低于该阈值时，发送最小流量警报。 将此值设置为0以禁用警报。 以每秒的请求数表示。 实值0或更大。

## AS::monitorAlertGenerator.minFreeHeapSpace — 可用堆空间阈值{#section-ce6705045f6842769030ccb1894594cc}

指定最小可用Java堆空间。 当可用堆空间低于此阈值时，将在Java垃圾收集周期之后立即发送优先级警报。 建议使用50 MB以安全运行平台服务器。 将可用堆空间保持在此值以上会降低垃圾收集周期的频率，这可能会提高整体服务器性能。 整数值（以字节为单位，0或更大）。

## AS::monitorAlertGenerator.maxOverlap — 并发请求的最大数{#section-ddc6925bff944758ab19bcc9cf3f2589}

当在平均间隔期间同时处理的平均请求数超过该阈值时，触发重叠警报。 高重叠可表示可能的服务器过载情况。

整数值1或更大。 典型范围是20到50，具体取决于缓存命中率和请求复杂度。

## AS::monitorAlertGenerator.lockedThreshold — 锁定请求阈值{#section-012a1c9937d445708380339279c62d80}

指定请求在被视为锁定或挂起之前必须挂起的秒数。 如果在平均间隔结束时至少一个请求被挂起的时间超过指定时间段，则发出锁定的请求警报。 正整数值（毫秒）。

要考虑涉及从外部HTTP服务器获取数据的复杂渲染请求和请求，建议将此值设置为至少30秒（除非此警报会检测到此情况）。
