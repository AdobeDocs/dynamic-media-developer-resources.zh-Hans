---
description: 使用这些服务器设置调试跟踪日志记录。
seo-description: 使用这些服务器设置调试跟踪日志记录。
seo-title: Debug_trace日志记录
solution: Experience Manager
title: Debug_trace日志记录
uuid: 33f1d093-007d-453b-965a-9d701a845954
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---


# Debug_trace日志记录{#debug-trace-logging}

使用这些服务器设置调试跟踪日志记录。

>[!NOTE]
>
>建议将所有日志文件配置为与`TC::directory`写入到同一文件夹。 这可确保所有映像服务日志文件都参与配置有`TC::maxDays`的自动日志文件旋转，这将防止由于磁盘空间不足而导致的潜在服务器不稳定。

## SV::log — 服务器主管跟踪日志文件路径{#section-3697bc480ff646e79cacc2812c55ef26}

服务器管理员日志文件的文件夹和基本文件名。 路径可以是绝对路径，也可以是相对于&#x200B;*[!DNL install_folder]*&#x200B;的路径。 服务器主管将在文件名（在文件后缀之前，如果有的话）后面附加连字符和当前日期(*[!DNL -yyyy-mm-dd]*)。 建议将所有日志文件发送到与平台服务器日志文件(`PS::LogFolder`)相同的文件夹，以利用平台服务器(`PS::LogDays`)实现的日志文件管理。 默认值为 [!DNL logs/Supervisor.log].

>[!NOTE]
>
>更改此设置前必须创建新文件夹。 确保已设置访问权限，以便服务器主管具有必要的创建、读取和写入权限。

## SV::tracelevel — 服务器主管跟踪日志级别{#section-36f8634741da4c618d67aa628b5fe474}

日志级别可以是1、2、3或4。 默认值为 2。

## IS::Log — 映像服务器调试日志文件路径{#section-73a3f09b77f2446c9f82207b7d8aec39}

图像服务器跟踪日志文件的文件夹和基本文件名。 路径可以是绝对路径，也可以是相对于&#x200B;*[!DNL install_folder]*&#x200B;的路径。 ImageServer将在文件名（在文件后缀之前，如果有的话）后面附加连字符和当前日期(*[!DNL -yyyy-mm-dd]*)。 建议将映像服务器日志文件发送到与平台服务器日志文件相同的文件夹(`PS::LogFolder`)以利用平台服务器实现的日志文件管理（请参阅`PS::LogDays`）。

>[!NOTE]
>
>更改此设置前必须创建新文件夹。 确保已设置访问权限，以便图像服务具有必要的创建、读取和写入权限。

## IS:TraceClient — 映像服务器调试日志级别{#section-3851f1f68e404430985c629ac80534db}

日志级别可以是1、2、3或4（默认为2）

1级记录与开始、关闭和平台服务器连接相关的事件。

级别2还记录与源映像的连接和断开连接。

级别3将像素数据请求的日志记录和像素数据的投放添加到平台服务器。

4级记录从平台服务器接收的所有消息。

级别3和级别4应仅用于调试目的，因为日志文件可能变得非常大。

## IS::TraceStatsInterval — 图像服务器统计日志间隔{#section-1d8df96d61044e33a5b2b2b0309c2d59}

图像服务器按此设置指定的时间间隔将内存统计信息写入其跟踪日志文件。 有效范围是5到86,400秒。
