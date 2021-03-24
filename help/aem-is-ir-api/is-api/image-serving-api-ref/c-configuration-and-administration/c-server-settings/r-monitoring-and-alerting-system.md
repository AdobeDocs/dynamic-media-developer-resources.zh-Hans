---
description: 使用这些服务器设置配置监视和警报系统。
solution: Experience Manager
title: 监视和警报系统
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---


# 监视和警报系统{#monitoring-and-alerting-system}

使用这些服务器设置配置监视和警报系统。

## AS::monitorAlertGenerator.enableGlobalAlerting — 警报系统启用{#section-612f8ea61794426ab205e22e5f665fa9}

通过设置为“true”并配置电子邮件通知设置来启用电子邮件通知。 设置为`false`将关闭所有电子邮件警报 — 这在使服务器离线进行维护时非常有用。 布尔值.

## AS::mailSender.host - SMTP主机{#section-151df07e7b44446581339bb7abeeba7a}

SMTP电子邮件服务器的IP地址。

## AS::mailSender.port- SMTP端口{#section-4b25efca8fd84d5c92dafacd0555e99d}

SMTP电子邮件服务器的监听端口。

## AS::monitorAlertGenerator.messageTo — 消息收件人{#section-0017bbaa15434117a70900c3f1163960}

应向其发送警报的一个或多个电子邮件地址。 使用分号作为分隔符。

## AS::monitorAlertGenerator.messageFrom — 消息发送者{#section-db320cba4ac2438ca1cfe6abce4aed87}

应在&#x200B;**[!UICONTROL From]**&#x200B;电子邮件字段中使用的电子邮件地址。

## AS::monitorAlertGenerator.alertInterval — 监视间隔{#section-99cb2e3380c1499e9d5aec3671ed73c7}

监控系统将在警报间隔期间累积警报条件并在每个间隔结束时发送包含所有累积警报的警报电子邮件。 毫秒、整数值、60000或更大。 通常设置为5或10分钟。

## AS::monitorAlertGenerator.heapSpaceResetInterval — 堆空间警报间隔{#section-fd5a2bf04ed44fdcaef20f77084151a8}

在发出堆空间警报之前的最短时间。 时间间隔（毫秒）。 整数值，0或更大。

## AS::monitorAlertGenerator.minTrafficForAlerts — 启用警报的最小流量{#section-8b4db2d6f96642309ca35c49eb3ab230}

每秒的请求数。 如果流量低于此阈值，则不会发出响应时间和错误警报。 设置为0可发送响应时间和错误警报，而不考虑流量。 实值0或更大。
