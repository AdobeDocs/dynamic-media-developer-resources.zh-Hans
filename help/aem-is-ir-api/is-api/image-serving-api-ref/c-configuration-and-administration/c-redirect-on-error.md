---
description: 可以将IS服务器配置为故障切换到备用服务器来处理涉及无法成功打开或读取的源映像的请求。
solution: Experience Manager
title: 出错时重定向
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# 出错时重定向{#redirect-on-error}

可以将IS服务器配置为故障切换到备用服务器来处理涉及无法成功打开或读取的源映像的请求。

重定向以下类型的请求：

* IS目录中的映像，但不在磁盘上的映像。

  如果图像不在目录中，则在找不到图像时不应发生错误重定向。

* 图像、颜色配置文件或字体损坏。
* 在磁盘上找不到静态内容。

  如果在磁盘上找不到静态内容请求，则会重定向该请求，即使引用的静态内容没有目录记录也是如此。

在其他任何情况下都不会发生错误重定向。

启用并在处理请求期间发生此类错误时，主服务器将请求发送到辅助服务器进行处理。 无论响应指示成功还是失败，该响应随后都直接转发到客户端。 主服务器使用缓存使用`REMOTE`标记此类转发请求的日志条目。 主服务器不会将响应数据缓存在本地。

通过将`PS::errorRedirect.rootUrl`设置为从属服务器的HTTP域名和端口号，启用错误重定向。 此外，连接超时配置为`PS::errorRedirect.connectTimeout`，而主服务器在向客户端返回错误之前等待辅助服务器响应的最长时间，配置为`PS::errorRedirect.socketTimeout`。

>[!NOTE]
>
>如果无法联系从属服务器，则即使配置了默认映像或错误映像，也会向客户端返回文本错误响应。

>[!NOTE]
>
>网络路径中的管道字符(|)不支持错误重定向。

## 另请参阅 {#section-2e8bfc128b944baf8108279d16492f3f}

[错误重定向](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
