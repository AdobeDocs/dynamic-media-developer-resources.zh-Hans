---
description: 图像蒙版。 请求遮罩(alpha渠道)数据。
seo-description: 图像蒙版。 请求遮罩(alpha渠道)数据。
seo-title: 遮罩
solution: Experience Manager
title: 遮罩
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# mask{#mask}

图像蒙版。 请求遮罩(alpha渠道)数据。

`req=mask`

服务器支持与相同的命 `req=img`令，并且由服务器以相同的方式进行处理，但服务器不返回RGB或RGBA数据，而是放弃颜色信息并仅返回蒙版(alpha渠道)数据。 回复数据格式和响应MIME类型由决定 `fmt=`。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.
