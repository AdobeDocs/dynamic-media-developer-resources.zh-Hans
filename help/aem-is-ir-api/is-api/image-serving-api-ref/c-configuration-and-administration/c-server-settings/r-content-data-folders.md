---
description: 对内容数据文件夹使用这些服务器设置。
seo-description: 对内容数据文件夹使用这些服务器设置。
seo-title: 内容数据文件夹
solution: Experience Manager
title: 内容数据文件夹
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---


# 内容数据文件夹{#content-data-folders}

对内容数据文件夹使用这些服务器设置。

## IS::RootPath — 图像数据根文件夹{#section-5c57569514bb4d00b19de31d2e137e3b}

所有源数据的位置，包括图像、字体和ICC用户档案。 这可以是相对于&#x200B;*[!DNL install_folder]*&#x200B;的一个或多个绝对文件路径或路径，以分号分隔。 如果为空，则&#x200B;*[!DNL install_folder]*&#x200B;是默认根。 可以指定多个值来跨多个文件系统分发图像数据。 图像服务器将按指定顺序尝试根路径，直到找到所请求的文件。

## PS::staticContent.rootPath — 静态内容数据根文件夹{#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

要通过[!DNL /is/static]上下文传送的静态内容源数据的位置。 可以是相对于&#x200B;*[!DNL install_folder]*&#x200B;的一个或多个绝对文件路径或路径，以分号分隔。 如果为空，则&#x200B;*[!DNL install_folder]*&#x200B;是默认根。

可以通过分号指定多个值并将静态内容分布到多个文件系统。 通常设置为与`IS::RootPath`相同的值。

平台服务器按指定的顺序尝试根路径，直到找到所请求的文件。

>[!NOTE]
>
>默认情况下，此字段有意设置为非现有位置([!DNL *[!DNL install_folder]*/static])，从而有效地禁用静态内容服务。

## IS::SaveDirectory — 文件保存根文件夹{#section-1c517f8d49ce4cb8b9013e520bf309c9}

`attribute::SavePath`的根路径（由`req=saveToFile`使用）。 图像服务器必须对要在其中创建图像文件的子文件夹具有创建访问权限。
