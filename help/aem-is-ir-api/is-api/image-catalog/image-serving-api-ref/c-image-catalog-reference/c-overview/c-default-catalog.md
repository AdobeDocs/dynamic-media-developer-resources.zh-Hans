---
description: 默认目录为所有图像目录的所有目录属性提供默认值。
solution: Experience Manager
title: 默认目录
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# 默认目录{#default-catalog}

默认目录为所有图像目录的所有目录属性提供默认值。

如果在特定图像目录中找不到特定属性，则服务器将改用默认目录中的相应值。 同样，默认目录可用于为特定目录数据记录(图像、宏定义、字体和ICC用户档案)提供默认值。 如果在特定图像目录中找不到特定数据记录，则服务器会尝试在默认目录中找到它。 这样，图像目录可以稀疏地填充，并简化全局属性和数据（如共享模板、宏、字体等）的管理。

此外，当操作中未涉及特定图像目录时，默认目录会提供所有属性和数据记录(宏、字体、ICC用户档案、请求预处理规则)。

要使平台服务器正常工作，默认目录的目录属性文件必须命名为[!DNL default.ini]，必须始终存在于目录文件夹中，并且必须完全填充所有必需属性，`attribute::RootId`和对各种目录数据文件的引用除外，这些属性都是可选的。

>[!NOTE]
>
>除[!DNL default.ini]之外的所有目录属性文件必须包含唯一的`attribute::RootId`值。 `attribute::RootId` in [!DNL default.ini] 必须为空。

