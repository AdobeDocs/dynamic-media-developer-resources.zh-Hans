---
description: 虽然添加新数据文件既简单又直接，但在替换服务器当前使用的现有数据文件时必须特别注意。 建议为替换文件指定一个新名称（例如，在文件名后附加一个版本后缀），而不是简单地替换此类文件。 新文件上线后，可以删除旧版本。
solution: Experience Manager
title: 删除或替换数据文件
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 删除或替换数据文件{#deleting-or-replacing-data-files}

虽然添加新数据文件既简单又直接，但在替换服务器当前使用的现有数据文件时必须特别注意。 建议为替换文件指定一个新名称（例如，在文件名后附加一个版本后缀），而不是简单地替换此类文件。 新文件上线后，可以删除旧版本。

>[!NOTE]
>
>在图像服务活动使用期间，不得替换或删除数据文件。 否则，可能会发生错误甚至服务器崩溃。

在所有情况下，请记住 [!DNL Platform Server] 在客户端看到更新的数据之前，缓存和客户端缓存条目必须失效。 可以使用 `cache=validate` 命令。

缓存管理器不会直接跟踪字体文件和ICC配置文件文件的更改。 如果在修改此类资源时未更改其ID，则服务器缓存将不会知晓更改， `cache=validate` 不会导致更新缓存条目。 `cache=update` 可用于强制重新生成此类缓存条目。

为避免替换文件的复杂情况，建议为替换文件指定一个新名称并更新相应的目录条目。 这将允许在服务器处于活动状态时替换任何数据文件，并导致服务器缓存条目立即失效而无需额外干预。 此方法可用于由图像目录管理的ICC配置文件、字体和所有图像。
