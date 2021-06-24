---
description: IS服务器可以配置为对于涉及源映像且无法成功打开或读取的请求，故障转移到备用服务器。
solution: Experience Manager
title: 出错时重定向
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# 出错时重定向{#redirect-on-error}

IS服务器可以配置为对于涉及源映像且无法成功打开或读取的请求，故障转移到备用服务器。

将重定向以下类型的请求：

* 是目录中的映像，但不在磁盘上。

   如果图像不在目录中，则在找不到图像时不应发生错误重定向。

* 图像、颜色配置文件或字体损坏。
* 在磁盘上找不到静态内容。

   在磁盘上找不到静态内容请求时，即使引用的静态内容没有目录记录，也会重定向静态内容请求。

在任何其他情况下都不会发生错误重定向。

启用后，如果在请求处理期间发生此类错误，主服务器将将请求发送到辅助服务器进行处理。 无论响应是指示成功还是失败，该响应随后都会直接转发给客户端。 主服务器使用`REMOTE`标记此类转发请求的日志条目。 响应数据不会由主服务器本地缓存。

通过将`PS::errorRedirect.rootUrl`设置为辅助服务器的HTTP域名和端口号，可启用错误重定向。 此外，连接超时配置为`PS::errorRedirect.connectTimeout`，并且主服务器在向客户端返回错误之前等待从从属服务器响应的最长时间配置为`PS::errorRedirect.socketTimeout`。

>[!NOTE]
>
>如果无法联系次服务器，则将向客户端返回文本错误响应，即使配置了默认图像或错误图像也是如此。

>[!NOTE]
>
>错误重定向不支持网络路径中的管道字符(|)。

## 另请参阅 {#section-2e8bfc128b944baf8108279d16492f3f}

[错误重定向](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
