---
description: 仅由 [!DNL Platform Server]访问静态内容源数据文件。
solution: Experience Manager
title: 静态内容源数据
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
TQID: 'https://experienceleague.adobe.com/XFhKuqGPsarkFZcYcBo7XuyCEsiJINf-o6koIZQKAXU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# 静态内容源数据{#static-content-source-data}

仅由[!DNL Platform Server]访问静态内容源数据文件。

静态内容数据文件的路径解析如下：

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

服务器将从右到左组合路径段，直到建立绝对文件路径。

所有` *[!DNL rootPath]*`区段都可为空、相对或绝对路径区段。

` *[!DNL catalogPath]*`是绝对或相对文件路径/名称。 *[!DNL requestPath]*&#x200B;必须为相对文件路径/名称。

可在[!DNL PlatformServer.conf]中定义多个`PS::staticContent.rootPaths`值。 这允许跨多个文件系统分发源数据文件。 [!DNL Platform Server]将按指定的顺序尝试备用路径，直到找到数据文件为止。
