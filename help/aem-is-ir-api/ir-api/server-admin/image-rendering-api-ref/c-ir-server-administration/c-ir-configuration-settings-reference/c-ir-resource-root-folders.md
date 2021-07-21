---
description: 以分号分隔的路径列表将用作具有相对文件路径的所有数据文件的根。
solution: Experience Manager
title: 资源根文件夹(ir.resourceRootPaths)
feature: Dynamic Media Classic，SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---

# 资源根文件夹(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

以分号分隔的路径列表将用作具有相对文件路径的所有数据文件的根。

可以是绝对路径，也可以是相对于&#x200B;*[!DNL install_folder]*&#x200B;的路径。 指定多个路径后，服务器将按给定顺序尝试每个根，直到找到文件为止。 默认为[!DNL ./resources]，默认根路径为[!DNL install_folder/resources]。
