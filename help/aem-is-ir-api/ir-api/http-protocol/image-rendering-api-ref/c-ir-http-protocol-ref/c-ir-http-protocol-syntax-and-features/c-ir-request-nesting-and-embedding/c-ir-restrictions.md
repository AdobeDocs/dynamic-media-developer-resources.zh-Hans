---
title: 限制
description: 对于嵌套和嵌入有一些限制。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# 限制{#restrictions}

对于嵌套和嵌入有一些限制。

为了使服务器具有良好的性能，嵌套请求返回的图像分辨率应该与材质所应用对象的纹理分辨率合理匹配。

外部图像缓存在本地。 只有在本地缓存条目失效后（基于expires HTTP标头），才会检测到对这些图像所做的任何更改。
