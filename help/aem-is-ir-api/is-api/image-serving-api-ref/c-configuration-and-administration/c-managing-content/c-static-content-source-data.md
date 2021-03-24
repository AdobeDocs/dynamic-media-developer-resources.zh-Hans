---
description: 静态内容源数据文件只能由平台服务器访问。
solution: Experience Manager
title: 静态内容源数据
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# 静态内容源数据{#static-content-source-data}

静态内容源数据文件只能由平台服务器访问。

静态内容数据文件的路径解析如下：

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

服务器从右到左组合路径段，直到建立绝对文件路径。

所有` *[!DNL rootPath]*`段都可以是空路径段、相对路径段或绝对路径段。

` *[!DNL catalogPath]*` 是绝对或相对文件路径/名称。*[!DNL requestPath]* 必须是相对文件路径/名称。

可以在[!DNL PlatformServer.conf]中定义多个`PS::staticContent.rootPaths`值。 这允许源数据文件跨多个文件系统分发。 平台服务器将按指定顺序尝试替代路径，直到找到数据文件。
