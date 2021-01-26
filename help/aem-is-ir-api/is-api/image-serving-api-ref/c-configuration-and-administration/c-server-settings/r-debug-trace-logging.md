---
description: 使用这些服务器设置调试跟踪记录。
seo-description: 使用这些服务器设置调试跟踪记录。
seo-title: 调试跟踪记录
solution: Experience Manager
title: 调试跟踪记录
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 33f1d093-007d-453b-965a-9d701a845954
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# Debug_trace日志记录{#debug-trace-logging}

使用这些服务器设置调试跟踪记录。

>[!NOTE]
>
>建议将所有日志文件配置为写入与`TC::directory`相同的文件夹。 这可确保所有映像服务日志文件都参与配置为`TC::maxDays`的自动日志文件旋转，这将防止由于磁盘空间不足而造成的潜在服务器不稳定。

## SV::log —— 服务器主管跟踪日志文件路径{#section-3697bc480ff646e79cacc2812c55ef26}

服务器管理员日志文件的文件夹和基本文件名。 路径可以是绝对路径，也可以是相对于&#x200B;*[!DNL install_folder]*&#x200B;的路径。 服务器主管将在文件名（在文件后缀之前，如果有）后附加连字符和当前日期(*[!DNL -yyyy-mm-dd]*)。 建议将所有日志文件发送到与平台服务器日志文件(`PS::LogFolder`)相同的文件夹，以利用平台服务器(`PS::LogDays`)实现的日志文件管理。 默认值为 [!DNL logs/Supervisor.log].

>[!NOTE]
>
>必须在更改此设置之前创建新文件夹。 确保已设置访问权限，以便服务器主管具有必要的创建、读取和写入权限。

## SV::tracelevel —— 服务器主管跟踪日志级别{#section-36f8634741da4c618d67aa628b5fe474}

日志级别可以是1、2、3或4。 默认值为 2。

## IS::Log - Image Server调试日志文件路径{#section-73a3f09b77f2446c9f82207b7d8aec39}

图像服务器跟踪日志文件的文件夹和基本文件名。 路径可以是绝对路径，也可以是相对于&#x200B;*[!DNL install_folder]*&#x200B;的路径。 ImageServer将在文件名（在文件后缀之前，如果有）后面附加连字符和当前日期(*[!DNL -yyyy-mm-dd]*)。 建议将映像服务器日志文件发送到与平台服务器日志文件相同的文件夹(`PS::LogFolder`)，以利用平台服务器实现的日志文件管理（请参阅`PS::LogDays`）。

>[!NOTE]
>
>必须在更改此设置之前创建新文件夹。 确保已设置访问权限，以便图像服务具有必要的创建、读取和写入权限。

## IS:TraceClient —— 映像服务器调试日志级别{#section-3851f1f68e404430985c629ac80534db}

日志级别可以是1、2、3或4（默认为2）

1级记录与开始、关闭和平台服务器连接相关的事件。

级别2还记录与源图像的连接和断开连接。

级别3将像素数据请求的记录和投放添加到平台服务器。

4级记录从平台服务器收到的所有消息。

级别3和级别4应仅用于调试目的，因为日志文件可能会变得非常大。

## IS::TraceStatsInterval —— 图像服务器统计日志时间间隔{#section-1d8df96d61044e33a5b2b2b0309c2d59}

图像服务器按此设置指定的时间间隔将内存统计信息写入其跟踪日志文件。 有效范围为5到86,400秒。
