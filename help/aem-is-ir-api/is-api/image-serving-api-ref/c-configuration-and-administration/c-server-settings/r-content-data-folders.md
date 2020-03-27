---
description: 将这些服务器设置用于内容数据文件夹。
seo-description: 将这些服务器设置用于内容数据文件夹。
seo-title: 内容数据文件夹
solution: Experience Manager
title: 内容数据文件夹
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 内容数据文件夹{#content-data-folders}

将这些服务器设置用于内容数据文件夹。

## IS::RootPath —— 图像数据根文件夹 {#section-5c57569514bb4d00b19de31d2e137e3b}

所有源数据的位置，包括图像、字体和ICC用户档案。 这可以是一个或多个相对的绝对文件路径或路径，以分 *[!DNL install_folder]*&#x200B;号分隔。 如果为空， *[!DNL install_folder]* 则为默认根。 可以指定多个值来跨多个文件系统分发图像数据。 图像服务器将按指定的顺序尝试根路径，直到找到所请求的文件。

## PS::staticContent.rootPath —— 静态内容数据根文件夹 {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

要通过上下文传送的静态内容源数据的位 [!DNL /is/static] 置。 可以是一个或多个相对的绝对文件路径或路径，以分 *[!DNL install_folder]*&#x200B;号分隔。 如果为空， *[!DNL install_folder]* 则为默认根。

可以通过分号指定多个值，并将静态内容分布到多个文件系统中。 通常设置为与相同的值 `IS::RootPath`。

平台服务器按指定的顺序尝试根路径，直到找到所请求的文件。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>默认情况下，此字段有意设置为非现有位置([!DNL *[!DNL install_folder]*/static])，从而有效地禁用静态内容服务。

## IS::SaveDirectory —— 文件保存根文件夹 {#section-1c517f8d49ce4cb8b9013e520bf309c9}

（由使用） `attribute::SavePath` 的根路 `req=saveToFile`径。 图像服务器必须对要在其中创建图像文件的子文件夹具有创建访问权限。
