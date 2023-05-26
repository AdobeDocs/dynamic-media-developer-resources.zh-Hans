---
description: 在服务器处于活动状态时，可以使用req=release命令在覆盖文件之前替换或删除晕影文件。
solution: Experience Manager
title: 删除或替换源数据文件
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# 删除或替换源数据文件{#deleting-or-replacing-source-data-files}

在服务器处于活动状态时，可以使用req=release命令在覆盖文件之前替换或删除晕影文件。

>[!NOTE]
>
>在渲染服务器访问数据文件时，不能替换或删除数据文件。

请记住，删除或替换源数据文件只会导致渲染服务器关闭该文件，直到访问该晕影的下一个请求为止。 如果文件使用率较高，可能需要多次重试。

必须停止渲染服务器才能替换其他数据文件。

[!DNL Platform Server] 替换材质文件或晕影时，缓存条目会自动失效。 替换ICC配置文件不会使缓存失效。

为避免替换文件时产生复杂情况，建议为替换文件提供一个新名称并更新相应的目录条目。 这允许在服务器处于活动状态时替换任何数据文件，并导致服务器缓存条目自动失效，而无需其他干预。 此方法可用于由图像目录管理的所有数据文件。
