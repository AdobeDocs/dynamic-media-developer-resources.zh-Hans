---
description: 使用这些服务器设置重定向错误。
solution: Experience Manager
title: 错误重定向
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# 错误重定向{#error-redirection}

使用这些服务器设置重定向错误。

>[!NOTE]
>
>网络路径中的管道字符(|)不支持错误重定向。

## PS：：errorRedirect.rootUrl — 重定向服务器 {#section-85f22e48d68842a490b0e1191543b558}

应将本地失败的请求重定向到的次映像服务部署的根URL ( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*])。 当此设置为空或未定义时，将禁用错误重定向（默认）。

## PS：：errorRedirect.connectTimeout — 重定向连接超时 {#section-3971be8f720d4b32a2cc7860b4085971}

在将错误返回到客户端之前，服务器等待与辅助服务器建立连接的最长时间（以毫秒为单位）。

## PS：：errorRedirect.socketTimeout — 重定向响应超时 {#section-69d8579f748d4044bca99dfb64dd523c}

服务器在放弃重定向请求并向客户端返回错误之前等待辅助服务器返回数据的最长时间（以毫秒为单位）。
