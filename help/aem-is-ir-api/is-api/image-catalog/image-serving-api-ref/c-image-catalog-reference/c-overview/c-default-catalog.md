---
description: 默认目录为所有图像目录的所有目录属性提供默认值。
solution: Experience Manager
title: 默认目录
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# 默认目录{#default-catalog}

默认目录为所有图像目录的所有目录属性提供默认值。

如果在特定图像目录中找不到特定属性，服务器将改用默认目录中的相应值。 同样，默认目录可用于为特定目录数据记录（图像、宏定义、字体和ICC配置文件）提供默认值。 如果在特定图像目录中找不到特定数据记录，则服务器会尝试在默认目录中查找该记录。 这允许稀疏填充图像目录，并简化全局属性和数据（如共享模板、宏、字体等）的管理。

此外，当操作中不包含特定的图像目录时，默认目录会提供所有属性和数据记录（宏、字体、ICC配置文件、请求预处理规则）。

为了正确运行 [!DNL Platform Server] 必须命名默认目录的目录属性文件 [!DNL default.ini]，必须始终存在于目录文件夹中，并且必须用所有必需的属性（不包括属性）完全填充 `attribute::RootId` 以及对各种目录数据文件的引用，所有这些都是可选的。

>[!NOTE]
>
>所有目录属性文件除外 [!DNL default.ini] 必须包含唯一的 `attribute::RootId` 值。 `attribute::RootId` 在 [!DNL default.ini] 必须为空。
