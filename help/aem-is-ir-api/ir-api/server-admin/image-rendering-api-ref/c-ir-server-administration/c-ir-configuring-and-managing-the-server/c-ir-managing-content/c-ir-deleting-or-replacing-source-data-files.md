---
description: 在服务器处于实时状态时，可以在文件被覆盖之前使用req=release命令替换或删除晕影文件。
solution: Experience Manager
title: 删除或替换源数据文件
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# 删除或替换源数据文件{#deleting-or-replacing-source-data-files}

在服务器处于实时状态时，可以在文件被覆盖之前使用req=release命令替换或删除晕影文件。

>[!NOTE]
>
>在呈现服务器访问数据文件时，不得替换或删除该数据文件。

请记住，删除或替换源数据文件只会导致呈现服务器关闭文件，直到下次请求访问该晕影为止。 如果文件被大量使用，则可能需要多次重试。

必须停止渲染服务器才能替换其他数据文件。

替换材料文件或晕影时，Platform Server缓存条目会自动失效。 替换ICC配置文件不会使缓存失效。

为避免替换文件的复杂情况，建议为替换文件指定一个新名称并更新相应的目录条目。 这允许在服务器处于活动状态时替换任何数据文件，并导致服务器缓存条目自动失效，无需额外干预。 此方法可用于由图像目录管理的所有数据文件。
