---
description: 虽然添加新数据文件简单明了，但在替换服务器正在使用的现有数据文件时必须特别小心。 建议为替换文件提供一个新名称（例如，在文件名后附加版本后缀），而不是简单地替换此类文件。 新文件上线后，可以删除旧版本。
solution: Experience Manager
title: 删除或替换数据文件
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# 删除或替换数据文件{#deleting-or-replacing-data-files}

虽然添加新数据文件简单明了，但在替换服务器正在使用的现有数据文件时必须特别小心。 建议为替换文件提供一个新名称（例如，在文件名后附加版本后缀），而不是简单地替换此类文件。 新文件上线后，可以删除旧版本。

>[!NOTE]
>
>数据文件决不应在由图像服务活动使用时替换或删除。 否则，可能会发生错误或甚至服务器崩溃。

在所有情况下，请记住，[!DNL Platform Server]缓存和客户端缓存项必须在客户端看到更新的数据之前失效。 可以使用`cache=validate`命令立即更新特定缓存项。

缓存管理器不会直接跟踪对字体文件和ICC配置文件所做的更改。 如果修改了此类资源而没有更改其ID，则服务器缓存不知道该更改，并且`cache=validate`不会导致缓存条目被更新。 `cache=update`可用于强制重新生成此类缓存条目。

为了避免替换文件带来的麻烦，建议为替换文件提供一个新名称并更新相应的目录条目。 这允许在服务器处于活动状态时替换任何数据文件，并导致服务器缓存条目立即失效，而无需其他干预。 此方法可用于ICC配置文件、字体和由图像目录管理的所有图像。
