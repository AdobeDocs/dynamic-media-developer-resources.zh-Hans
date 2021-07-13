---
description: 常规服务器设置
solution: Experience Manager
title: 常规
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---

# 常规{#general}

常规服务器设置

## TC::PsPort — 主侦听端口 {#section-d31d3051aa994a76b60b70c3d9f7e89f}

指定平台服务器的主侦听端口。 此端口还用于访问图像提供、图像渲染和Dynamic Media查看器（如果已安装）的文档和示例页面。

## IS::CacheServerUrl — 缓存服务根Url {#section-bcca227a1f91453b834db4ea050968e2}

指定允许图像服务器访问缓存服务的HTTP根路径。 必须设置为[!DNL http://localhost:TC::PsPort /is/cache/secondary]，端口号与`TC::PsPort`匹配。

## IS::RemoteUrlDefaultExpiration — 远程Image Source默认TTL {#section-e4c31228b459492cacd2f482d9575f71}

使用`src={…}`结构通过HTTP从远程源获取的缓存图像的TTL。 仅当远程服务器的HTTP响应中不包含过期标头时使用。 整数值（以秒为单位）。

## IS::RemoteUrlTimeout — 远程Image Source超时 {#section-437646c479cc4bea81dae42100a3c50a}

图像服务器在返回错误之前将等待远程服务器通过HTTP传送请求的图像文件的时间。 整数值（以秒为单位）。

## PS::allowDefaultCatalogRequests — 启用/禁用默认目录请求 {#section-484e442a115a49b4ac269d1718b351e1}

设置为false可禁止在路径中不包含有效目录ID的请求。 默认值为 `true`. 如果设置为`false`，则对于没有目录ID的请求，会返回错误。

>[!NOTE]
>
>`req=catalogprops` 不受此设置的约束。

## PS::saveToFile.saveTimeout — 文件保存超时 {#section-d22afd8ad86144b28684ed95a59db40e}

未指定`timeout=`时`req=saveToFile`的默认超时值。 `msec`. 如果未在指定的时间段内完成保存操作，则将返回错误。
