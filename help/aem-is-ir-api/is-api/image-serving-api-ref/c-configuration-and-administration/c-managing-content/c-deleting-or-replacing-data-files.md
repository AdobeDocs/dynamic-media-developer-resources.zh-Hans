---
description: 虽然添加新数据文件简单明了，但在替换服务器主动使用的现有数据文件时必须特别小心。 建议为替换文件提供一个新名称（例如，在文件名后附加版本后缀），而不是简单地替换此类文件。 新文件上线后，可以删除旧版本。
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

虽然添加新数据文件简单明了，但在替换服务器主动使用的现有数据文件时必须特别小心。 建议为替换文件提供一个新名称（例如，在文件名后附加版本后缀），而不是简单地替换此类文件。 新文件上线后，可以删除旧版本。

>[!NOTE]
>
>数据文件在图像服务处于活跃使用状态时绝不能替换或删除。 否则，可能会发生错误或甚至服务器崩溃。

在所有情况下，请记住 [!DNL Platform Server] 缓存和客户端缓存条目必须失效后，客户端才能看到更新的数据。 可以使用立即更新特定的缓存条目 `cache=validate` 命令。

缓存管理器不会直接跟踪对字体文件和ICC配置文件所做的更改。 如果修改了此类资源而没有更改其ID，则服务器缓存将不会知道此更改，并且 `cache=validate` 不会导致缓存条目更新。 `cache=update` 可用于强制重新生成此类缓存条目。

为避免替换文件时产生复杂情况，建议为替换文件提供一个新名称并更新相应的目录条目。 这将允许在服务器处于活动状态时替换任何数据文件，并导致服务器缓存条目立即失效，而无需其他干预。 此方法可用于ICC配置文件、字体和由图像目录管理的所有图像。
