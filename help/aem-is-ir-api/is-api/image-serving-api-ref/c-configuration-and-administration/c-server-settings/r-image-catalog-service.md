---
description: 将这些服务器设置用于图像目录服务。
solution: Experience Manager
title: 图像目录服务
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
TQID: 'https://experienceleague.adobe.com/Fs2xGD3Dpd8pe5jtto4kPMF0BrJiLNRvdBn8RSPiQjw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 197
ht-degree: 0%

---

# 图像目录服务{#image-catalog-service}

将这些服务器设置用于图像目录服务。

## CS：：catalog.rootPath — 图像目录文件夹 {#section-02d107f157384b18835f884f24fea3aa}

图像目录文件夹的位置（必须包含所有[!DNL catalog.ini]文件）。 可以是绝对文件路径或相对于&#x200B;*[!DNL install_folder]*&#x200B;的路径。 服务器持续监视此文件夹，并在检测到新的主目录文件（具有[!DNL .ini]文件后缀）或现有主目录文件的最后修改时间已更改时，加载或重新加载目录。

## CS：：catalog.cacheRoot — 目录缓存文件夹 {#section-73e499c3a5974f1aa4251e70272ff503}

目录系统缓存的根文件夹。 可设置为与`PS::cache.rootPaths`中的某个文件夹相同。 在更改此设置之前，必须手动创建文件夹。

## CS：：catalog.modificationWaitTime — 目录文件分析延迟 {#section-7348065bcc124cb68ea947bf1b9b0845}

在更改[!DNL catalog.ini]文件之后目录服务等待的时间（毫秒），直到加载辅助目录文件为止。 这种延迟有助于确保所有辅助目录文件在目录服务尝试加载它们之前都是最新的。 以毫秒为单位的整数值。

## CS：：catalog.refreshInterval — 目录文件检查频率 {#section-517fefc1d8784777a1026abec8630d58}

目录服务检查图像目录更改的频率。 以毫秒为单位的整数值。
