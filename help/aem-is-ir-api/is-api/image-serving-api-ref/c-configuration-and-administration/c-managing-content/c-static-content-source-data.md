---
description: 静态内容源数据文件只能由 [!DNL Platform Server].
solution: Experience Manager
title: 静态内容源数据
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# 静态内容源数据{#static-content-source-data}

静态内容源数据文件只能由 [!DNL Platform Server].

静态内容数据文件的路径解析如下：

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

服务器将从右到左组合路径段，直到建立绝对文件路径。

全部 ` *[!DNL rootPath]*` 区段可以为空、相对或绝对路径区段。

` *[!DNL catalogPath]*` 是绝对或相对文件路径/名称。 *[!DNL requestPath]* 必须为相对文件路径/名称。

多个 `PS::staticContent.rootPaths` 值可在以下位置定义 [!DNL PlatformServer.conf]. 这允许跨多个文件系统分发源数据文件。 此 [!DNL Platform Server] 按指定的顺序尝试备用路径，直到找到数据文件为止。
