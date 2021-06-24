---
description: 所有日志文件都写入到TC目录指定的同一日志文件夹中。
solution: Experience Manager
title: 服务器日志记录
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# 服务器日志记录{#server-logging}

所有日志文件都写入到TC::directory指定的同一日志文件夹中。

日志文件通常每天创建和旋转。 在指定的天数(`TC::maxDays`)后，将自动删除日志文件夹中较旧的日志文件。

重要信息必须为日志文件保留足够的磁盘空间，以避免磁盘空间耗尽。 对于使用频繁的服务器和默认日志设置，可能需要1-2 GB/天。

平台服务器和图像服务器会创建下面描述的三种类型的日志文件。

其他图像服务组件和某些其他Dynamic Media包(如Dynamic Media查看器)也可能在同一文件夹中创建日志文件。 这些日志文件供Dynamic Media内部使用，Dynamic Media技术支持可能会出于故障排除目的而请求使用这些日志文件。

* [访问日志](c-access-log.md)
* [跟踪日志](c-trace-log.md)
* [图像服务器日志](c-image-server-log.md)

## 另请参阅 {#section-5ff5e46031b1461c92de24e632610d6d}

[访问日志记录](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f)、 [调试/跟踪日志记录](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
