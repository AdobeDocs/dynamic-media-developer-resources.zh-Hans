---
description: 使用这些服务器设置重定向错误。
seo-description: 使用这些服务器设置重定向错误。
seo-title: 错误重定向
solution: Experience Manager
title: 错误重定向
uuid: b2c2f725-98c3-44a4-8f50-2ca4da7f2156
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# 重定向错误{#error-redirection}

使用这些服务器设置重定向错误。

>[!NOTE]
>
>错误重定向不支持网络路径中的管道字符(|)。

## PS::errorRedirect.rootUrl — 重定向服务器{#section-85f22e48d68842a490b0e1191543b558}

根URL([!DNL HTTP:// *[!DNL domain]*[:*[!DNL port]*])，用于应将本地失败的请求重定向到的次映像服务部署。 当此设置为空或未定义时，将禁用错误重定向（默认）。

## PS::errorRedirect.connectTimeout — 重定向连接超时{#section-3971be8f720d4b32a2cc7860b4085971}

服务器将等待与辅助服务器建立连接的最长时间（以毫秒为单位），然后将错误返回给客户端。

## PS::errorRedirect.socketTimeout — 重定向响应超时{#section-69d8579f748d4044bca99dfb64dd523c}

服务器将等待辅助服务器返回数据的最长时间（以毫秒为单位），然后放弃重定向请求并将错误返回到客户端。
