---
description: 大多数材料都可以动态着色。
solution: Experience Manager
title: 着色材料
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# 着色材料{#colorizing-materials}

大多数材料都可以动态着色。

着色算法简单，对色调范围有限的材料图像效果最好。 要对材料着色，渲染器只需减去`bgc=`值，并将`color=`值添加到每个像素值。

如果未指定`color=`，则禁用着色。 `bgc=` 被橱柜材料忽视；将改用文件中嵌入 [!DNL vnc] 的基色值。
