---
title: 着色材料
description: 大多数材料都可以动态着色。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
TQID: 'https://experienceleague.adobe.com/MGmuOj214tFPKeSGwz33pGn2m0B0fme1Cq-umlxG9v0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# 着色材料{#colorizing-materials}

大多数材料都可以动态着色。

彩色化算法简单，对色调范围有限的材质图像效果最好。 为了给材质着色，渲染器仅需减去`bgc=`值，并将`color=`值添加到每个像素值。

如果未指定`color=`，则禁用彩色化。 `bgc=`特性被文件柜材料忽略；改用嵌入到[!DNL vnc]文件中的基色值。
