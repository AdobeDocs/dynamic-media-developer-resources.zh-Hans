---
description: 所有日志文件都写入使用TC目录指定的同一日志文件夹中。
solution: Experience Manager
title: 服务器日志记录
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# 服务器日志记录{#server-logging}

所有日志文件都写入使用TC：：directory指定的同一日志文件夹中。

日志文件通常每天创建和轮换。 在指定的天数(`TC::maxDays`)后，日志文件夹中的旧日志文件将自动删除。

重要信息必须为日志文件保留足够的磁盘空间，以避免磁盘空间不足。 使用量大的服务器和默认日志设置可能需要1-2 GB/天。

[!DNL Platform Server]和映像服务器创建下面描述的三种类型的日志文件。

其他图像服务组件和某些其他Dynamic Media包(如Dynamic Media查看器)也可能会在同一文件夹中创建日志文件。 这些日志文件供Dynamic Media内部使用，Dynamic Media技术支持可能会请求这些文件以进行故障排除。

* [访问日志](c-access-log.md)
* [跟踪日志](c-trace-log.md)
* [图像服务器日志](c-image-server-log.md)

## 另请参阅 {#section-5ff5e46031b1461c92de24e632610d6d}

[访问日志记录](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f)，[调试/跟踪日志记录](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
