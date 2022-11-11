---
description: 将这些服务器设置用于内容数据文件夹。
solution: Experience Manager
title: 内容数据文件夹
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# 内容数据文件夹{#content-data-folders}

将这些服务器设置用于内容数据文件夹。

## IS::RootPath — 图像数据根文件夹 {#section-5c57569514bb4d00b19de31d2e137e3b}

所有源数据（包括图像、字体和ICC配置文件）的位置。 这可以是相对于 *[!DNL install_folder]*，以分号分隔。 如果为空， *[!DNL install_folder]* 是默认根。 可以指定多个值来跨多个文件系统分发图像数据。 图像服务器将按照指定的顺序尝试根路径，直到找到请求的文件为止。

## PS::staticContent.rootPath — 静态内容数据根文件夹 {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

要通过 [!DNL /is/static] 上下文。 可以是相对于 *[!DNL install_folder]*，以分号分隔。 如果为空， *[!DNL install_folder]* 是默认根。

可以通过分号指定多个值并分隔这些值，以在多个文件系统中分发静态内容。 通常设置为与 `IS::RootPath`.

的 [!DNL Platform Server] 会按指定的顺序尝试根路径，直到找到请求的文件。

>[!NOTE]
>
>默认情况下，此字段被有意设置为非现有位置([!DNL *[!DNL install_folder]*/static])，从而有效地禁用静态内容服务。

## IS::SaveDirectory — 文件保存根文件夹 {#section-1c517f8d49ce4cb8b9013e520bf309c9}

的根路径 `attribute::SavePath` (使用 `req=saveToFile`)。 图像服务器必须具有为其创建图像文件的子文件夹创建访问权限。
