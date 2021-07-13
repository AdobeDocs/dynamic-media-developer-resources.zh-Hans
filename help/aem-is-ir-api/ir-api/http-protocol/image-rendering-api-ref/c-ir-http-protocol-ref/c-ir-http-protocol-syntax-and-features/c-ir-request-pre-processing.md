---
description: 图像渲染基于正则表达式匹配和替换规则提供了一个简单的请求预处理器。
solution: Experience Manager
title: 请求预处理*
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# 请求预处理*{#request-pre-processing}

图像渲染基于正则表达式匹配和替换规则提供了一个简单的请求预处理器。

规则集合（规则集）可以附加到每个物料目录，包括默认目录。 规则由XML格式的文件指定。

请求预处理规则可以在请求的路径和查询部分由图像渲染解析器处理之前对其进行修改，包括处理路径、添加命令、更改命令值以及应用模板或宏。 规则还可用于配置和覆盖某些通常仅通过目录属性控制的功能，例如设置默认回复图像大小或将HTTP服务限制为特定客户端IP地址。

请求预处理规则适用于各种应用程序，其中一些应用程序如下所示：

* 实施&#x200B;*虚拟路径*&#x200B;机制，该机制允许将请求路径重新映射到文件、FTP和HTTP路径。
* 禁止使用CPU密集型命令来防止服务器滥用。
* 根据请求路径或图像名称控制图像质量设置（如JPEG质量或锐化）。

有关创建、使用和管理规则集的详细信息，请参阅规则集参考。

另请参阅规则集引用，属性：:RuleSetFile
