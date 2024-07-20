---
description: 使用这些服务器设置设置设置映像大小限制。
solution: Experience Manager
title: 图像大小限制
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 1%

---

# 图像大小限制{#image-size-limits}

使用这些服务器设置设置设置映像大小限制。

## IS：：MaxMessageSize — 响应大小限制 {#section-bd942385d4d144cd904003695d72c85e}

限制允许图像服务器发送到[!DNL Platform Server]的数据大小。 实际上，这限制了“图像服务”可以通过HTTP (MB)方式返回到客户端的编码/压缩响应图像的大小。

## IS：：MaxRenderRgnPixels — 输出图像大小限制 {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

限制图像服务器可以生成的图像大小（不包括保存到文件的图像）。 大于0的整数值（百万像素）。 如果渲染操作超出大小限制，则返回错误。 默认值为 16。

## IS：：MaxSavePixels — 用于保存到文件的大小限制 {#section-d1547c4afa88467080ab08356f775e06}

使用`req=saveToFile`命令限制图像服务器写入文件的图像大小。 大于0的整数值（百万像素）。 如果文件保存操作超过该限制，则会返回错误。 默认值为1亿像素。

## IS：：MaxNonDsfSize — 非PTIFF输入图像的大小限制 {#section-50de28a7158a436393cce5da0d1e4d46}

允许图像服务器打开的不是PTIFF的图像的最大尺寸（以像素为单位）。 当尝试访问大于此限制的非PTIFF图像时，图像服务返回错误。

>[!NOTE]
>
>如果将此值设置得过高，可能会导致图像服务器内存不足，并导致故障，包括崩溃。
