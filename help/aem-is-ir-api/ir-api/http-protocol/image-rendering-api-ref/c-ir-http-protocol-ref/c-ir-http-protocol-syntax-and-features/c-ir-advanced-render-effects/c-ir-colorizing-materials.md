---
description: 大多数材料都可以动态着色。
seo-description: 大多数材料都可以动态着色。
seo-title: 着色材料
solution: Experience Manager
title: 着色材料
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---


# 着色材料{#colorizing-materials}

大多数材料都可以动态着色。

彩色化算法简单，对于色相范围有限的材料图像效果最好。 要对材料着色，渲染器只需减去`bgc=`值并将`color=`值添加到每个像素值。

如果未指定`color=`，则禁用着色。 `bgc=` 被橱柜材料忽视；而是使用嵌入在文件 [!DNL vnc] 中的基色值。
