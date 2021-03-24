---
description: 嵌套和嵌入有一些限制。
solution: Experience Manager
title: 限制
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# 限制{#restrictions}

嵌套和嵌入有一些限制。

为了获得良好的服务器性能，嵌套请求返回的图像分辨率应与应用素材的对象的纹理分辨率合理匹配。

外部图像将本地缓存。 仅当本地缓存条目失效（基于过期的HTTP头）后，才会检测对此类图像所做的任何更改。
