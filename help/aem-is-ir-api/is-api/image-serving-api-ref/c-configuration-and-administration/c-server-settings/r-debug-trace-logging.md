---
description: 使用这些服务器设置调试跟踪日志记录。
solution: Experience Manager
title: Debug_trace日志记录
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---

# Debug_trace日志记录{#debug-trace-logging}

使用这些服务器设置调试跟踪日志记录。

>[!NOTE]
>
>建议将所有日志文件配置为写入与相同的文件夹 `TC::directory`. 这可确保所有图像服务日志文件都参与配置了的自动日志文件轮换 `TC::maxDays`，这将防止因磁盘空间不足而导致的潜在服务器不稳定。

## SV：：log — 服务器监控器跟踪日志文件路径 {#section-3697bc480ff646e79cacc2812c55ef26}

Server Supervisor日志文件的文件夹和基本文件名。 路径可以是绝对路径或相对路径 *[!DNL install_folder]*. Server Supervisor将附加一个连字符和当前日期( *[!DNL -yyyy-mm-dd]*)到文件名（在文件后缀之前，如果有）。 建议将所有日志文件发送到 [!DNL Platform Server] 日志文件( `PS::LogFolder`)以利用由实现的日志文件管理 [!DNL Platform Server] ( `PS::LogDays`)。 默认值为 [!DNL logs/Supervisor.log].

>[!NOTE]
>
>在更改此设置之前，必须创建新文件夹。 确保设置了访问权限，以便Server Supervisor具有必要的创建、读取和写入权限。

## SV：：tracelevel — 服务器监控器跟踪日志级别 {#section-36f8634741da4c618d67aa628b5fe474}

日志级别可以是1、2、3或4。 默认值为 2。

## IS：：Log — 图像服务器调试日志文件路径 {#section-73a3f09b77f2446c9f82207b7d8aec39}

映像服务器跟踪日志文件的文件夹和基本文件名。 路径可以是绝对路径或相对路径 *[!DNL install_folder]*. ImageServer将附加一个连字符和当前日期( *[!DNL -yyyy-mm-dd]*)到文件名（在文件后缀之前，如果有）。 建议将图像服务器日志文件发送到 [!DNL Platform Server] 日志文件( `PS::LogFolder`)以利用由实现的日志文件管理 [!DNL Platform Server] (请参阅 `PS::LogDays`)。

>[!NOTE]
>
>在更改此设置之前，必须创建新文件夹。 确保设置了访问权限，以便图像服务具有必要的创建、读取和写入权限。

## IS：TraceClient — 图像服务器调试日志级别 {#section-3851f1f68e404430985c629ac80534db}

日志级别可以是1、2、3或4（默认值为2）

第1级记录与启动、关闭和关闭相关的事件 [!DNL Platform Server] 连接。

级别2还记录与源映像的连接和断开连接。

第3级添加了像素数据请求的日志记录并将其提交到 [!DNL Platform Server].

第4级记录从 [!DNL Platform Server].

级别3和4应仅用于调试目的，因为日志文件可能会变得非常大。

## IS：：TraceStatsInterval — 图像服务器统计信息日志间隔 {#section-1d8df96d61044e33a5b2b2b0309c2d59}

图像服务器将内存统计信息写入其跟踪日志文件，其间隔为此设置所指定的时间间隔。 有效范围为5到86,400秒。
