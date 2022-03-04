---
title: 限制
description: 嵌套和嵌入存在一些限制。
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

嵌套和嵌入存在一些限制。

为了获得良好的服务器性能，嵌套请求返回的图像分辨率应与正在应用材料的对象的纹理分辨率合理匹配。

外来图像缓存在本地。 只有在本地缓存条目失效（基于过期的HTTP标头）后，才会检测到对此类图像的任何更改。
