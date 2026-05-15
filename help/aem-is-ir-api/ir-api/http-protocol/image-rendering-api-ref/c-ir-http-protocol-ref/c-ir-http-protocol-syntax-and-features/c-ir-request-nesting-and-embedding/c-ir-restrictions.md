---
title: 限制
description: 对于嵌套和嵌入有一些限制。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
TQID: 'https://experienceleague.adobe.com/rwy6ZnKA0pc-z-dqhsI0gD-FSqpqZr1bcIgJqtsjfIs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 0%

---

# 限制{#restrictions}

对于嵌套和嵌入有一些限制。

为了使服务器具有良好的性能，嵌套请求返回的图像分辨率应该与材质所应用对象的纹理分辨率合理匹配。

外部图像缓存在本地。 只有在本地缓存条目失效后（基于expires HTTP标头），才会检测到对这些图像所做的任何更改。
