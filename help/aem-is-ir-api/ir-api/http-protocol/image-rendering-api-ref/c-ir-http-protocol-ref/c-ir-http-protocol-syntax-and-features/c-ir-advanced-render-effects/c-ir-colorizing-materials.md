---
title: 着色材料
description: 大多数材料都可以动态着色。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# 着色材料{#colorizing-materials}

大多数材料都可以动态着色。

彩色化算法简单，对色调范围有限的材质图像效果最好。 为了给材质着色，渲染器仅需减去`bgc=`值，并将`color=`值添加到每个像素值。

如果未指定`color=`，则禁用彩色化。 `bgc=`特性被文件柜材料忽略；改用嵌入到[!DNL vnc]文件中的基色值。
