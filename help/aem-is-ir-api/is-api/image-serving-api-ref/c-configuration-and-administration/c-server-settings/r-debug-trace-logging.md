---
description: 使用这些服务器设置来调试跟踪日志记录。
solution: Experience Manager
title: Debug_trace日志记录
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Debug_trace日志记录{#debug-trace-logging}

使用这些服务器设置来调试跟踪日志记录。

>[!NOTE]
>
>建议将所有日志文件配置为与`TC::directory`写入到同一文件夹。 这可确保所有图像服务日志文件都参与配置了`TC::maxDays`的自动日志文件旋转，这将防止由于磁盘空间不足情况而导致的潜在服务器不稳定。

## SV::log — 服务器主管跟踪日志文件路径 {#section-3697bc480ff646e79cacc2812c55ef26}

服务器管理员日志文件的文件夹和基本文件名。 路径可以是绝对路径，也可以是相对于&#x200B;*[!DNL install_folder]*&#x200B;的路径。 服务器管理员将在文件名（在文件后缀之前，如果有）后附加连字符和当前日期(*[!DNL -yyyy-mm-dd]*)。 建议将所有日志文件发送到与Platform Server日志文件(`PS::LogFolder`)相同的文件夹，以利用Platform Server(`PS::LogDays`)实施的日志文件管理。 默认值为 [!DNL logs/Supervisor.log].

>[!NOTE]
>
>必须先创建新文件夹，然后才能更改此设置。 确保已设置访问权限，以便服务器主管具有必要的创建、读取和写入权限。

## SV::tracelevel — 服务器主管跟踪日志级别 {#section-36f8634741da4c618d67aa628b5fe474}

日志级别可以是1、2、3或4。 默认值为 2。

## IS::Log - Image Server调试日志文件路径 {#section-73a3f09b77f2446c9f82207b7d8aec39}

图像服务器跟踪日志文件的文件夹和基本文件名。 路径可以是绝对路径，也可以是相对于&#x200B;*[!DNL install_folder]*&#x200B;的路径。 ImageServer将在文件名后面附加一个连字符和当前日期(*[!DNL -yyyy-mm-dd]*)（在文件后缀之前，如果有）。 建议将图像服务器日志文件发送到与Platform Server日志文件(`PS::LogFolder`)相同的文件夹，以利用Platform Server实施的日志文件管理（请参阅`PS::LogDays`）。

>[!NOTE]
>
>必须先创建新文件夹，然后才能更改此设置。 确保设置了访问权限，以便图像服务具有必要的创建、读取和写入权限。

## IS:TraceClient — 图像服务器调试日志级别 {#section-3851f1f68e404430985c629ac80534db}

日志级别可以是1、2、3或4（默认为2）

级别1记录与启动、关闭和Platform Server连接相关的事件。

级别2还会记录与源映像的连接和断开连接。

级别3添加了像素数据请求的日志记录并将其提交到Platform Server。

第4级记录从平台服务器收到的所有消息。

级别3和级别4应仅用于调试目的，因为日志文件可能会变得非常大。

## IS::TraceStatsInterval — 图像服务器统计信息日志时间间隔 {#section-1d8df96d61044e33a5b2b2b0309c2d59}

图像服务器将内存统计信息以此设置指定的间隔写入其跟踪日志文件。 有效时间范围为5到86,400秒。
