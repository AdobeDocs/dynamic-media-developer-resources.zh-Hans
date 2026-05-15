---
description: 常规服务器设置
solution: Experience Manager
title: 常规
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
TQID: 'https://experienceleague.adobe.com/hjww7EYpf4xNxpUFQ1fudMOqNtokgykthwhonn78ZFE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# 常规{#general}

常规服务器设置

## TC：：PsPort — 主侦听端口 {#section-d31d3051aa994a76b60b70c3d9f7e89f}

指定[!DNL Platform Server]的主侦听端口。 此端口还用于访问图像提供、图像渲染和Dynamic Media查看器（如果已安装）的文档和示例页面。

## IS：：CacheServerUrl — 缓存服务根Url {#section-bcca227a1f91453b834db4ea050968e2}

指定HTTP根路径，以允许图像服务器访问缓存服务。 必须设置为[!DNL http://localhost:TC::PsPort /is/cache/secondary]，端口号与`TC::PsPort`匹配。

## IS：：RemoteUrlDefaultExpiration — 远程Image Source默认TTL {#section-e4c31228b459492cacd2f482d9575f71}

使用`src={…}`构造从远程源通过HTTP获取的缓存图像的TTL。 仅当远程服务器的HTTP响应中不包含过期标头时使用。 以秒为单位的整数值。

## IS：：RemoteUrlTimeout — 远程Image Source超时 {#section-437646c479cc4bea81dae42100a3c50a}

在返回错误之前，图像服务器等待远程服务器通过HTTP传递所请求的图像文件的时间。 以秒为单位的整数值。

## PS：：allowDefaultCatalogRequests — 启用/禁用默认目录请求 {#section-484e442a115a49b4ac269d1718b351e1}

设置为false可不允许在路径中未包含有效目录ID的请求。 默认值为`true`。 当设置为`false`时，将为没有目录ID的请求返回错误。

>[!NOTE]
>
>`req=catalogprops`不受此设置限制。

## PS：：saveToFile.saveTimeout — 文件保存超时 {#section-d22afd8ad86144b28684ed95a59db40e}

未指定`timeout=`时`req=saveToFile`的默认超时值。 `msec`. 如果未在指定的时间内完成保存操作，则会返回错误。
