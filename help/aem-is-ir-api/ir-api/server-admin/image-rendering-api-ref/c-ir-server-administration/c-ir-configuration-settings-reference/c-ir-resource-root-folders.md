---
title: 资源根文件夹(ir.resourceRootPaths)
description: 以分号分隔的路径列表用作具有相对文件路径的所有数据文件的根。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
TQID: 'https://experienceleague.adobe.com/5mKCVHonfG4riWoIenUyFHtMnSg3cmL-Lm-YTGN34fA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 84
ht-degree: 0%

---

# 资源根文件夹(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

以分号分隔的路径列表用作具有相对文件路径的所有数据文件的根。

它可以是绝对路径或相对于&#x200B;*[!DNL install_folder]*&#x200B;的路径。 指定多个路径时，服务器会按指定顺序尝试每个根，直到找到文件为止。 默认根路径[!DNL install_folder/resources]的默认值为[!DNL ./resources]。
