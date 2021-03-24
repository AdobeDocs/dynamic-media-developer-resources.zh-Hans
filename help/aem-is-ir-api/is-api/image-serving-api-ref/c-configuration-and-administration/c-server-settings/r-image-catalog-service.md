---
description: 对图像目录服务使用这些服务器设置。
solution: Experience Manager
title: 图像目录服务
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# 图像目录服务{#image-catalog-service}

对图像目录服务使用这些服务器设置。

## CS::catalog.rootPath - Image Catalog文件夹{#section-02d107f157384b18835f884f24fea3aa}

图像目录文件夹的位置（所有[!DNL catalog.ini]文件必须位于其中）。 可以是绝对文件路径或相对于&#x200B;*[!DNL install_folder]*&#x200B;的路径。 当检测到新的主目录文件（具有[!DNL .ini]文件后缀）或现有主目录文件的上次修改时间发生更改时，服务器会持续监视此文件夹并加载或重新加载目录。

## CS::catalog.cacheRoot — 目录缓存文件夹{#section-73e499c3a5974f1aa4251e70272ff503}

目录系统缓存的根文件夹。 可以设置为与`PS::cache.rootPaths`中的某个文件夹相同。 更改此设置之前，必须手动创建文件夹。

## CS::catalog.modificationWaitTime — 目录文件解析延迟{#section-7348065bcc124cb68ea947bf1b9b0845}

目录服务在[!DNL catalog.ini]文件发生更改后等待的时间（以毫秒为单位），直到它加载辅助目录文件。 此延迟有助于确保所有辅助目录文件在目录服务尝试加载它们之前都是最新的。 整数值（毫秒）。

## CS::catalog.refreshInterval — 目录文件检查频率{#section-517fefc1d8784777a1026abec8630d58}

目录服务检查图像目录更改的频率。 整数值（毫秒）。
