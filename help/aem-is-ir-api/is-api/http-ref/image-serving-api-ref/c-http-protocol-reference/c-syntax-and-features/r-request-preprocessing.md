---
description: 图像服务根据正则表达式匹配和替换规则提供了一个简单的请求预处理器。
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

图像服务根据正则表达式匹配和替换规则提供了一个简单的请求预处理器。

可以将规则集合（规则集）附加到每个图像目录，包括默认目录。 使用XML格式的文件指定规则。

在[!DNL Platform Server]的解析器处理请求之前，请求预处理规则可以修改请求的路径和查询部分，包括处理路径、添加命令、更改命令值以及应用模板或宏。 规则还可用于配置和覆盖某些安全功能，这些功能通常仅通过目录属性进行控制，例如请求模糊处理、水标记，以及将HTTP服务限制到特定客户端IP地址。

请求预处理规则适用于多种应用程序，其中一些应用程序如下所示：

* 实施&#x200B;*虚拟路径*&#x200B;机制，该机制允许将请求路径重新映射到文件、FTP和HTTP路径。
* 选择性地强制实施按图像名称或路径过滤的安全功能，例如水印。
* 从特定IP地址访问服务器时省略水印或其他安全功能。
* 强制将命令（如`defaultImage=`）应用于所有请求或在URL路径或查询字符串中显示特定模式的请求。
* 不允许使用占用大量CPU的命令来防止服务器滥用。
* 允许源图像位于HTTP或FTP服务器上，同时仍在请求路径上指定源图像，而不是通过`src=`指定。
* 根据请求路径或图像名称控制图像质量设置(例如JPEG质量或锐化)。

有关创建、使用和管理规则集的详细信息，请参阅[规则集引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)。

## 另请参阅 {#see-also}

[规则集引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)，[属性：：RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
