---
description: 静态内容源数据文件仅由平台服务器访问。
solution: Experience Manager
title: 静态内容源数据
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# 静态内容源数据{#static-content-source-data}

静态内容源数据文件仅由平台服务器访问。

静态内容数据文件的路径解析如下：

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

服务器从右到左组合路径段，直到建立绝对文件路径。

所有` *[!DNL rootPath]*`区段都可以是空、相对或绝对路径区段。

` *[!DNL catalogPath]*` 是绝对或相对文件路径/名称。*[!DNL requestPath]* 必须是相对文件路径/名称。

可以在[!DNL PlatformServer.conf]中定义多个`PS::staticContent.rootPaths`值。 这允许源数据文件跨多个文件系统分发。 平台服务器将按照指定的顺序尝试替代路径，直到找到数据文件为止。
