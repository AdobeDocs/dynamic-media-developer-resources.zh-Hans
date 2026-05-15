---
description: 默认目录为所有图像目录的所有目录属性提供默认值。
solution: Experience Manager
title: 默认目录
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
TQID: 'https://experienceleague.adobe.com/qbfEwBJ-eQmCbBR0MJQhP7x3ZEd30nfLJHWjBVoXIjc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 0%

---

# 默认目录{#default-catalog}

默认目录为所有图像目录的所有目录属性提供默认值。

如果在特定图像目录中找不到特定属性，服务器将改用默认目录中的相应值。 同样，默认目录可用于为特定目录数据记录（图像、宏定义、字体和ICC配置文件）提供默认值。 如果在特定图像目录中找不到特定数据记录，则服务器会尝试在默认目录中查找该记录。 这允许稀疏填充图像目录，并简化全局属性和数据（如共享模板、宏、字体等）的管理。

此外，当操作中不包含特定的图像目录时，默认目录将提供所有属性和数据记录（宏、字体、ICC配置文件、请求预处理规则）。

为了使[!DNL Platform Server]正确运行，默认目录的目录属性文件必须命名为[!DNL default.ini]，必须始终存在于目录文件夹中，并且必须使用所有必需的属性完全填充，不包括`attribute::RootId`和对各种目录数据文件的引用，所有这些都是可选的。

>[!NOTE]
>
>除[!DNL default.ini]之外的所有目录属性文件都必须包含唯一的`attribute::RootId`值。 [!DNL default.ini]中的`attribute::RootId`必须为空。
