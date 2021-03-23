---
description: 在服务器处于实时状态时，可以使用req=release命令替换或删除晕影文件，而文件正好被覆盖。
seo-description: 在服务器处于实时状态时，可以使用req=release命令替换或删除晕影文件，而文件正好被覆盖。
seo-title: 删除或替换源数据文件
solution: Experience Manager
title: 删除或替换源数据文件
uuid: 13dc0489-7ab0-481e-b213-214affe9819e
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# 删除或替换源数据文件{#deleting-or-replacing-source-data-files}

在服务器处于实时状态时，可以使用req=release命令替换或删除晕影文件，而文件正好被覆盖。

>[!NOTE]
>
>在渲染服务器访问数据文件时，不得替换或删除该数据文件。

请记住，删除或替换源数据文件只会导致渲染服务器关闭文件，直到下次请求访问该晕影时为止。 如果文件被大量使用，则可能需要多个重试。

必须停止渲染服务器以替换其他数据文件。

替换材料文件或晕影时，平台服务器缓存条目会自动失效。 替换ICC用户档案文件不会使缓存失效。

为避免替换文件的复杂性，建议为替换文件指定新名称并更新相应的目录条目。 这允许在服务器处于活动状态时替换任何数据文件，并导致服务器缓存条目自动失效而无需额外干预。 此方法可用于由图像目录管理的所有数据文件。
