---
title: Debug_trace日志记录
description: 使用这些服务器设置调试跟踪日志记录。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Debug_trace日志记录{#debug-trace-logging}

使用这些服务器设置调试跟踪日志记录。

>[!NOTE]
>
>Adobe建议您将所有日志文件配置为写入与`TC::directory`相同的文件夹。 这样做可确保所有图像服务日志文件都参与使用`TC::maxDays`配置的自动日志文件旋转，从而防止因磁盘空间不足而导致的服务器不稳定。

## SV：：log — 服务器主管跟踪日志文件路径 {#section-3697bc480ff646e79cacc2812c55ef26}

Server Supervisor日志文件的文件夹和基本文件名。 路径可以是绝对路径或相对于&#x200B;*[!DNL install_folder]*&#x200B;的路径。 服务器主管将连字符和当前日期(*[!DNL -yyyy-mm-dd]*)附加到文件名（在文件后缀之前，如果有的话）。 Adobe建议将所有日志文件发送到[!DNL Platform Server]日志文件(`PS::LogFolder`)所在的文件夹，以使用[!DNL Platform Server] (`PS::LogDays`)实施的日志文件管理。 默认值为[!DNL logs/Supervisor.log]。

>[!NOTE]
>
>在更改此设置之前，必须创建新文件夹。 确保设置访问权限，以便服务器主管具有必要的创建、读取和写入权限。

## SV：：tracelevel — 服务器主管跟踪日志级别 {#section-36f8634741da4c618d67aa628b5fe474}

日志级别可以是1、2、3或4。 默认值为 2。

## IS：：Log — 映像服务器调试日志文件路径 {#section-73a3f09b77f2446c9f82207b7d8aec39}

映像服务器跟踪日志文件的文件夹和基本文件名。 路径可以是绝对路径或相对于&#x200B;*[!DNL install_folder]*&#x200B;的路径。 ImageServer将连字符和当前日期(*[!DNL -yyyy-mm-dd]*)附加到文件名（在文件后缀之前，如果有的话）。 Adobe建议您将图像服务器日志文件发送到与[!DNL Platform Server]日志文件(`PS::LogFolder`)相同的文件夹，以使用由[!DNL Platform Server]实现的日志文件管理（请参阅`PS::LogDays`）。

>[!NOTE]
>
>在更改此设置之前，必须创建新文件夹。 确保设置了访问权限，以便图像服务具有必要的创建、读取和写入权限。

## IS:TraceClient — 映像服务器调试日志级别 {#section-3851f1f68e404430985c629ac80534db}

日志级别可以是1、2、3或4（默认值为2）

级别1记录与启动、关闭和[!DNL Platform Server]连接相关的事件。

级别2还记录与源映像的连接和断开连接。

级别3添加对像素数据的请求日志记录并将其投放到[!DNL Platform Server]。

级别4记录从[!DNL Platform Server]接收的所有消息。

级别3和级别4应仅用于调试目的，因为日志文件可能会变得很大。

## IS：：TraceStatsInterval — 图像服务器统计信息日志时间间隔 {#section-1d8df96d61044e33a5b2b2b0309c2d59}

映像服务器将内存统计信息写入其跟踪日志文件，其间隔为此设置指定。 有效范围为5-86,400秒。
