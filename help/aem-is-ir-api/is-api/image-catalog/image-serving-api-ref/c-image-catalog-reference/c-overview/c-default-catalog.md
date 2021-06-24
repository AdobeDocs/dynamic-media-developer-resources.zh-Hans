---
description: 默认目录为所有图像目录的所有目录属性提供默认值。
solution: Experience Manager
title: 默认目录
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# 默认目录{#default-catalog}

默认目录为所有图像目录的所有目录属性提供默认值。

如果在特定图像目录中找不到特定属性，则服务器将改用默认目录中的相应值。 同样，默认目录可用于为特定目录数据记录（图像、宏定义、字体和ICC配置文件）提供默认值。 如果在特定图像目录中找不到特定数据记录，则服务器会尝试在默认目录中查找该数据记录。 这样，图像目录便可以稀疏填充，并简化全局属性和数据（如共享模板、宏、字体等）的管理。

此外，当操作中未涉及特定图像目录时，默认目录会提供所有属性和数据记录（宏、字体、ICC配置文件、请求预处理规则）。

为了使Platform Server正常运行，默认目录的目录属性文件必须命名为[!DNL default.ini]，必须始终存在于目录文件夹中，并且必须完全填充所有必需属性，不包括`attribute::RootId`和对各种目录数据文件的引用，这些属性都是可选的。

>[!NOTE]
>
>除[!DNL default.ini]之外的所有目录属性文件都必须包含唯一的`attribute::RootId`值。 `attribute::RootId` 中 [!DNL default.ini] 的必须为空。
