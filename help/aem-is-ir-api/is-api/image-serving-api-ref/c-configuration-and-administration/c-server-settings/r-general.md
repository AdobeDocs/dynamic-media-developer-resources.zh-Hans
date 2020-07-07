---
description: 常规服务器设置
seo-description: 常规服务器设置
seo-title: 常规
solution: Experience Manager
title: 常规
topic: Scene7 Image Serving - Image Rendering API
uuid: d7ec3dba-64b8-431b-b446-84ab6139ba8a
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 2%

---


# 常规{#general}

常规服务器设置

## TC::PsPort —— 主监听端口 {#section-d31d3051aa994a76b60b70c3d9f7e89f}

指定平台服务器的主侦听端口。 此端口还用于访问图像服务、图像渲染和Scene7查看器（如果已安装）的文档和示例页面。

## IS::CacheServerUrl —— 缓存服务根Url {#section-bcca227a1f91453b834db4ea050968e2}

指定允许图像服务器访问缓存服务的HTTP根路径。 必须设置为， [!DNL http://localhost:TC::PsPort /is/cache/secondary]并且端口号匹配 `TC::PsPort`。

## IS::RemoteUrlDefaultExpiration —— 远程图像源默认TTL {#section-e4c31228b459492cacd2f482d9575f71}

通过HTTP从远程源使用构造获得的缓存图像的TTL `src={…}` 。 仅在远程服务器的HTTP响应中不包含Expiration头时使用。 整数值（以秒为单位）。

## IS::RemoteUrlTimeout —— 远程映像源超时 {#section-437646c479cc4bea81dae42100a3c50a}

映像服务器等待远程服务器通过HTTP传送请求的图像文件的时间，然后返回错误。 整数值（以秒为单位）。

## PS::allowDefaultCatalogRequests —— 启用／禁用默认目录请求 {#section-484e442a115a49b4ac269d1718b351e1}

设置为false可禁止路径中不包含有效目录id的请求。 默认值为 `true`. 如果设置为 `false`，则对于没有目录ID的请求将返回错误。

>[!NOTE]
>
>`req=catalogprops` 不受此设置的约束。

## PS::saveToFile.saveTimeout —— 文件保存超时 {#section-d22afd8ad86144b28684ed95a59db40e}

未指定时的 `req=saveToFile` 默 `timeout=`认超时值。 `msec`. 如果在指定的时间内未完成保存操作，则将返回错误。
