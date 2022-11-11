---
description: 图像提供基于正则表达式匹配和替换规则的简单请求预处理器。
solution: Experience Manager
title: 请求预处理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# 请求预处理{#request-preprocessing}

图像提供基于正则表达式匹配和替换规则的简单请求预处理器。

规则集合（规则集）可以附加到每个图像目录，包括默认目录。 规则由XML格式的文件指定。

请求预处理规则可以修改请求的路径和查询部分，然后再由 [!DNL Platform Server]的解析器，包括处理路径、添加命令、更改命令值以及应用模板或宏。 规则还可用于配置和覆盖某些安全功能，这些功能通常仅通过目录属性进行控制，例如请求模糊处理、水标记，以及将HTTP服务限制为特定的客户端IP地址。

请求预处理规则适用于各种应用程序，其中一些应用程序如下所示：

* 实施 *虚拟路径* 机制，允许将请求路径重映射到文件、FTP和HTTP路径。
* 有选择地实施按图像名称或路径过滤的安全功能，如水印。
* 在从特定IP地址访问服务器时省略水印或其他安全功能。
* 强制应用命令，例如 `defaultImage=`、到所有请求或URL路径或查询字符串中显示特定模式的请求。
* 不允许使用CPU密集型命令来防止服务器滥用。
* 允许源图像位于HTTP或FTP服务器上，同时仍在请求路径上指定它们，而不是通过 `src=`.
* 根据请求路径或图像名称控制图像质量设置(如JPEG质量或锐化)。

有关创建、使用和管理规则集的详细信息，请参阅 [规则集引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## 另请参阅 {#see-also}

[规则集引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [属性：:RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
