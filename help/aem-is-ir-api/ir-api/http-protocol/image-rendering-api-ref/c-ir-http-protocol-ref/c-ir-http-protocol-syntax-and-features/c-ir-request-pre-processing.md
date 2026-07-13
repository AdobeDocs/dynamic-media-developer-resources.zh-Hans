---
title: 请求预处理
description: 图像渲染提供了一个基于正则表达式匹配和替换规则的简单请求预处理程序。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
TQID: 'https://experienceleague.adobe.com/zs4izZzuO7u6wYOPmdd8AT7r4q-cUFXWUlB1MW6aV0Y'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 0%

---

# 请求预处理{#request-pre-processing}

图像渲染提供了一个基于正则表达式匹配和替换规则的简单请求预处理程序。

可以将规则集合（规则集）附加到每个材料目录，包括默认目录。 使用XML格式的文件指定规则。

请求预处理规则可以在图像渲染解析器处理请求之前修改请求的路径和查询部分。 此方案包括处理路径、添加命令、更改命令值以及应用模板或宏。 规则还可用于配置和覆盖某些通常仅通过目录属性控制的功能，例如设置默认回复图像大小或将HTTP服务限制到特定客户端IP地址。

请求预处理规则适用于各种应用程序，下面列出了其中一些应用程序：

* 实施&#x200B;*虚拟路径*&#x200B;机制，该机制允许将请求路径重新映射到文件、FTP和HTTP路径。
* 禁止使用CPU密集型命令以防止服务器滥用。
* 根据请求路径或图像名称控制图像质量设置（例如JPEG质量或锐化）。

有关创建、使用和管理规则集的详细信息，请参阅规则集参考。

另请参阅规则集引用，属性：：RuleSetFile

