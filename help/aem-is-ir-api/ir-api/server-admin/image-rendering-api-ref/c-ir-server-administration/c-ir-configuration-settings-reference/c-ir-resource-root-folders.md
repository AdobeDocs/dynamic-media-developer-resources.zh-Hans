---
description: 列表路径（用分号分隔）用作具有相对文件路径的所有数据文件的根。
solution: Experience Manager
title: 资源根文件夹(ir.resourceRootPaths)
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# 资源根文件夹(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

列表路径（用分号分隔）用作具有相对文件路径的所有数据文件的根。

可以是相对于&#x200B;*[!DNL install_folder]*&#x200B;的绝对路径或路径。 指定多个路径后，服务器将按给定顺序尝试每个根，直到找到文件。 默认值为[!DNL ./resources]，默认根路径为[!DNL install_folder/resources]。
