---
title: 请求预处理
description: 图像渲染提供了一种基于正则表达式匹配和替换规则的简单请求预处理器。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
source-git-commit: 20f4922402bd31c71ae650a01597b574220809fa
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# 请求预处理{#request-pre-processing}

图像渲染提供了一种基于正则表达式匹配和替换规则的简单请求预处理器。

可以将规则集合（规则集）附加到每个材料目录，包括默认目录。 使用XML格式的文件指定规则。

请求预处理规则可以在图像渲染解析器处理请求之前修改请求的路径和查询部分。 此方案包括处理路径、添加命令、更改命令值以及应用模板或宏。 规则还可用于配置和覆盖某些通常仅通过目录属性控制的功能，例如设置默认回复图像大小或将HTTP服务限制为特定客户端IP地址。

请求预处理规则适用于各种应用程序，其中一些应用程序如下所示：

* 实施 *虚拟路径* 机制，允许将请求路径重新映射到文件、FTP和HTTP路径。
* 不允许使用占用大量CPU的命令来防止服务器滥用。
* 根据请求路径或图像名称控制图像质量设置(例如JPEG质量或锐化)。

有关创建、使用和管理规则集的详细信息，请参阅规则集参考。

另请参阅规则集引用，属性：：RuleSetFile
