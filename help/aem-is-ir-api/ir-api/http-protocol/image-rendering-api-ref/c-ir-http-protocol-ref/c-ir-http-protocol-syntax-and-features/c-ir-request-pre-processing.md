---
description: “图像渲染”提供基于常规表达式匹配和替换规则的简单请求预处理器。
seo-description: “图像渲染”提供基于常规表达式匹配和替换规则的简单请求预处理器。
seo-title: 请求预处理*
solution: Experience Manager
title: 请求预处理*
uuid: ef69ea23-753c-40c8-9edd-eab9c8820c98
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# 请求预处理*{#request-pre-processing}

“图像渲染”提供基于常规表达式匹配和替换规则的简单请求预处理器。

规则集合（规则集）可附加到每个材料目录，包括默认目录。 规则是使用XML格式的文件指定的。

请求预处理规则可以修改请求的路径和查询部分，然后再由图像渲染分析器处理它们，包括操作路径、添加命令、更改命令值以及应用模板或宏。 规则还可用于配置和覆盖某些通常仅通过目录属性控制的功能，例如设置默认的回复图像大小或将HTTP服务限制为特定客户端IP地址。

请求预处理规则适用于各种应用程序，其中一些如下所示：

* 实施&#x200B;*虚拟路径*&#x200B;机制，允许将请求路径重新映射到文件、FTP和HTTP路径。
* 不允许使用占用大量CPU的命令以防止服务器滥用。
* 根据请求路径或图像名称控制图像质量设置（如JPEG质量或锐化）。

有关创建、使用和管理规则集的详细信息，请参阅规则集参考。

另请参阅规则集引用，属性：:RuleSetFile
