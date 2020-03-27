---
description: 图像服务基于常规表达式匹配和替换规则提供简单的请求处理器。
seo-description: 图像服务基于常规表达式匹配和替换规则提供简单的请求处理器。
seo-title: 请求预处理
solution: Experience Manager
title: 请求预处理
topic: Scene7 Image Serving - Image Rendering API
uuid: 375bbca2-7a4a-49a9-9577-86e6b2f19990
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 请求预处理{#request-preprocessing}

图像服务基于常规表达式匹配和替换规则提供简单的请求处理器。

规则集合（规则集）可以附加到每个图像目录，包括默认目录。 规则由XML格式的文件指定。

请求预处理规则可以在请求的路径和查询部分由平台服务器的分析器处理之前对其进行修改，包括操作路径、添加命令、更改命令值以及应用模板或宏。 规则还可用于配置和覆盖某些安全功能，这些功能通常仅通过目录属性进行控制，例如请求模糊化、水印标记以及将HTTP服务限制到特定客户端IP地址。

请求预处理规则适用于各种应用程序，其中一些如下所示：

* 实施虚 *拟路径机制* ，该机制允许将请求路径重新映射到文件、FTP和HTTP路径。
* 有选择地强制使用安全功能，如按图像名称或路径过滤的水印。
* 从特定IP地址访问服务器时省略水印或其他安全功能。
* 将命令（如）强制应 `defaultImage=`用到所有请求或URL路径或查询字符串中显示特定模式的请求。
* 不允许使用占用大量CPU的命令来防止服务器滥用。
* 允许源图像位于HTTP或FTP服务器上，同时仍在请求路径上指定它们，而不是与一起指定 `src=`。
* 根据请求路径或图像名称控制图像质量设置（如JPEG质量或锐化）。

有关创建、使用和管理规则集的详细信息，请参阅规则集 [参考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)。

## 另请参阅 {#see-also}

[规则集引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [属性：:RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
