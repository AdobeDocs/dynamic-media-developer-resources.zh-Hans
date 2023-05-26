---
description: 对图像目录服务使用这些服务器设置。
solution: Experience Manager
title: 图像目录服务
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---

# 图像目录服务{#image-catalog-service}

对图像目录服务使用这些服务器设置。

## CS：：catalog.rootPath — 图像目录文件夹 {#section-02d107f157384b18835f884f24fea3aa}

图像目录文件夹的位置(其中 [!DNL catalog.ini] 必须找到文件)。 可以是绝对文件路径或相对于 *[!DNL install_folder]*. 服务器持续监视此文件夹，并在新的主目录文件(具有 [!DNL .ini] 文件后缀)，或者现有主目录文件的最后修改时间已更改时。

## CS：：catalog.cacheRoot — 目录缓存文件夹 {#section-73e499c3a5974f1aa4251e70272ff503}

目录系统缓存的根文件夹。 可以设置为与中的文件夹之一相同 `PS::cache.rootPaths`. 在更改此设置之前，必须手动创建文件夹。

## CS：：catalog.modificationWaitTime — 目录文件解析延迟 {#section-7348065bcc124cb68ea947bf1b9b0845}

目录服务在之后等待的时间（毫秒） [!DNL catalog.ini] 文件会一直更改，直到加载辅助目录文件为止。 这种延迟有助于确保所有辅助目录文件在目录服务尝试加载之前都是最新的。 以毫秒为单位的整数值。

## CS：：catalog.refreshInterval — 目录文件检查频率 {#section-517fefc1d8784777a1026abec8630d58}

目录服务检查图像目录更改的频率。 以毫秒为单位的整数值。
