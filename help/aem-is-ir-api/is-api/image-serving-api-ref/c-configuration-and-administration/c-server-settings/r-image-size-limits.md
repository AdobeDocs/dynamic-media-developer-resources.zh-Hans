---
description: 使用这些服务器设置设置图像大小限制。
seo-description: 使用这些服务器设置设置图像大小限制。
seo-title: 图像大小限制
solution: Experience Manager
title: 图像大小限制
uuid: 6736e652-c495-45a2-bdd2-9975f99af0a2
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---


# 图像大小限制{#image-size-limits}

使用这些服务器设置设置图像大小限制。

## IS::MaxMessageSize — 响应大小限制{#section-bd942385d4d144cd904003695d72c85e}

限制允许图像服务器发送到平台服务器的数据大小。 这有效地限制了图像服务可以通过HTTP(MB)返回到客户端的编码/压缩响应图像的大小。

## IS::MaxRenderRgnPixels — 输出图像大小限制{#section-868ceb9764dd42dfb133ffeb72f9d3fb}

限制图像服务器可以生成的图像的大小（不包括保存到文件的图像）。 大于0的整数值（以百万像素为单位）。 如果渲染操作超过大小限制，则返回错误。 默认值为 16。

## IS::MaxSavePixels — 保存到文件{#section-d1547c4afa88467080ab08356f775e06}的大小限制

使用`req=saveToFile`命令限制图像服务器将写入文件的图像大小。 大于0的整数值（以百万像素为单位）。 如果文件保存操作超过该限制，则返回错误。 默认为1亿像素。

## IS::MaxNonDsfSize — 非PTIFF输入图像的大小限制{#section-50de28a7158a436393cce5da0d1e4d46}

允许图像服务器打开的非PTIFF图像的最大大小（以M像素为单位）。 尝试访问大于此限制的非PTIFF图像时，图像服务将返回一个错误。

>[!NOTE]
>
>将此值设置得太高可能会导致图像服务器内存不足，并导致故障（包括崩溃）。

