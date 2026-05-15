---
title: 不同材质不透明度
description: 实色和应用于重叠对象的可重复纹理以及小贴片和窗口覆盖材料均支持可变不透明度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
TQID: 'https://experienceleague.adobe.com/i4d6vy62vn9BfFrS2W0srO671N9Ad4hCUXR7J4cajJA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 0%

---

# 不同材质不透明度{#varying-material-opacity}

实色和应用于重叠对象的可重复纹理以及小贴片和窗口覆盖材料均支持可变不透明度。

不透明度信息可以简单地通过使用带有Alpha通道的RGB图像来提供。 此外，可以使用`opacity=`命令更改整体不透明度（适用于RGB和RGBA图像）。

墙边框还支持RGBA图像，主要支持管芯切割边框。

定义窗口覆盖的[!DNL vnw]文件可以包含不透明度渠道。 它由渲染器与可重复纹理的alpha通道和`opacity=`值组合在一起，以提供用于透明和半透明窗口处理的完整的不透明度效果。
