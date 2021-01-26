---
description: 可以将IS服务器配置为对涉及源映像的请求故障切换到替代服务器，而源映像无法成功打开或读取。
seo-description: 可以将IS服务器配置为对涉及源映像的请求故障切换到替代服务器，而源映像无法成功打开或读取。
seo-title: 错误时重定向
solution: Experience Manager
title: 错误时重定向
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 894babe9-9c3c-4972-ae8f-387d65b4167d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---


# 重定向到错误{#redirect-on-error}

可以将IS服务器配置为对涉及源映像的请求故障切换到替代服务器，而源映像无法成功打开或读取。

将重定向以下类型的请求：

* IS映像位于目录中，但不在磁盘上。

   如果图像不在目录中，则在找不到图像时不会发生错误重定向。

* 损坏图像、颜色用户档案或字体。
* 在磁盘上找不到静态内容。

   在磁盘上找不到静态内容请求时，即使引用的静态内容没有目录记录，也会重定向静态内容请求。

在任何其他情况下都不会发生错误重定向。

当启用请求时，当在请求处理过程中发生此类错误时，主服务器将将请求发送给从属服务器进行处理。 无论响应是否表示成功或失败，都会直接转发给客户端。 主服务器使用缓存`REMOTE`标记此类转发请求的日志条目。 响应数据不由主服务器本地缓存。

通过将`PS::errorRedirect.rootUrl`设置为辅助服务器的HTTP域名和端口号，可启用错误重定向。 此外，连接超时配置为`PS::errorRedirect.connectTimeout`，主服务器在将错误返回到客户端之前等待从从属服务器响应的最长时间配置为`PS::errorRedirect.socketTimeout`。

>[!NOTE]
>
>如果无法联系从属服务器，则即使配置了默认图像或错误图像，也会向客户端返回文本错误响应。

>[!NOTE]
>
>错误重定向不支持网络路径中的管道字符(|)。

## 另请参阅 {#section-2e8bfc128b944baf8108279d16492f3f}

[错误重定向](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
