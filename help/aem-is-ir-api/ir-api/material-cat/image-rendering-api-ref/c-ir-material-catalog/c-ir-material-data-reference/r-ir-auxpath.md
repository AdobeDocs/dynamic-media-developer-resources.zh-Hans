---
description: 数据文件路径。 与此图像关联的非图像数据文件的相对路径和名称。
solution: Experience Manager
title: 辅助路径
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55f82596-72f0-48c4-9b3a-f10ea5f610f1
TQID: 'https://experienceleague.adobe.com/p1AZ2QZmQpKM9D-gvBCxavzsdWlLjb-MSO-kluc05oE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 3%

---

# 辅助路径{#auxpath}

数据文件路径。 与此图像关联的非图像数据文件的相对路径和名称。

服务器将此值与attribute：：RootPath结合使用，以构建实际的文件路径。 也可以是绝对文件路径。

用于为封包材料指定封包样式文件，或为窗口覆盖材料指定窗口覆盖样式文件。 留空则保留所有其他材料。

## 属性 {#section-4268350054b7421da0ce0327f0731a52}

文本字符串值。 如果指定，则必须是有效的相对或绝对文件路径。 机箱材料和窗户覆盖材料所需。 对于所有其他材料，必须为空。

## 默认 {#section-287005c2d8e948fa958f69ba7b90b437}

无。

## 另请参阅 {#section-e1f7a61c00d04a80af28e2e67481ab92}

[attribute：：RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) ， [catalog：：Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590)， [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)

