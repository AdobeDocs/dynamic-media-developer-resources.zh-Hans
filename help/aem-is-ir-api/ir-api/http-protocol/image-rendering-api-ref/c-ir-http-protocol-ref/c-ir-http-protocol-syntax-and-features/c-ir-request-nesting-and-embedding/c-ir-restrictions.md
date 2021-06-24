---
description: 嵌套和嵌入存在一些限制。
solution: Experience Manager
title: 限制
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# 限制{#restrictions}

嵌套和嵌入存在一些限制。

为了获得良好的服务器性能，嵌套请求返回的图像分辨率应与正在应用材料的对象的纹理分辨率合理匹配。

外来图像缓存在本地。 只有在本地缓存条目失效（基于过期的HTTP标头）后，才会检测到对此类图像的任何更改。
