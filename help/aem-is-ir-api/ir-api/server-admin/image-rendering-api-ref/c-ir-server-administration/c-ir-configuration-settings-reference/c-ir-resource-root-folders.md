---
title: 资源根文件夹(ir.resourceRootPaths)
description: 以分号分隔的路径列表用作具有相对文件路径的所有数据文件的根。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# 资源根文件夹(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

以分号分隔的路径列表用作具有相对文件路径的所有数据文件的根。

它可以是绝对路径或相对于&#x200B;*[!DNL install_folder]*&#x200B;的路径。 指定多个路径时，服务器会按指定顺序尝试每个根，直到找到文件为止。 默认根路径[!DNL install_folder/resources]的默认值为[!DNL ./resources]。
