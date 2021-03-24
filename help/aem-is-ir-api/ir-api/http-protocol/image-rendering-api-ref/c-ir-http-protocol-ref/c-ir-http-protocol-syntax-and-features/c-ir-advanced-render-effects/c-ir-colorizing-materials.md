---
description: 大多数材料都可以动态着色。
solution: Experience Manager
title: 着色材料
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# 着色材料{#colorizing-materials}

大多数材料都可以动态着色。

彩色化算法简单，对于色相范围有限的材料图像效果最好。 要对材料着色，渲染器只需减去`bgc=`值并将`color=`值添加到每个像素值。

如果未指定`color=`，则禁用着色。 `bgc=` 被橱柜材料忽视；而是使用嵌入在文件 [!DNL vnc] 中的基色值。
