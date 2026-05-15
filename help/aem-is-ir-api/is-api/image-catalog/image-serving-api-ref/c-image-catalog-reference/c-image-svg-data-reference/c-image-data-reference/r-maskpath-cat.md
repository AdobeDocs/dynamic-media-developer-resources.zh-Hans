---
description: 遮罩文件路径。 与此目录记录关联的蒙版图像文件的相对或绝对路径和名称。
solution: Experience Manager
title: 蒙版路径
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
TQID: 'https://experienceleague.adobe.com/tUXD-vnkr3qkaH3B-dE-e9wfSPXAcnwRbqG9KuJej9E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 175
ht-degree: 2%

---

# 蒙版路径{#maskpath}

遮罩文件路径。 与此目录记录关联的蒙版图像文件的相对或绝对路径和名称。

允许将单独的蒙版附加到图像。

服务器使用[管理Source数据](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md)中描述的路径解析规则来查找数据文件。

## 属性 {#section-cdc3b7e2811e41008479cd97887c01b7}

文本字符串值。 可选. 如果已指定，则必须是有效的相对或绝对图像服务器文件路径。 如果没有文件后缀，则会附加`attribute::DefaultExt`。

如果在目录记录中定义了主图像(`catalog::Path`)和蒙版图像(`catalog::MaskPath`)，则两者必须具有完全相同的像素大小。 蒙版图像必须为8位灰度。

请求中的`mask=`覆盖`catalog::MaskPath`。

`catalog::MaskPath`覆盖主图像(`catalog::Path`)中的Alpha通道（如果存在），并且未关联Alpha通道（即未预乘）。 如果对图像alpha进行预乘，则忽略`catalog::MaskPath`并始终使用alpha通道。

## 默认 {#section-78533e35bfec469ba087cb68a35bb81b}

无。

## 另请参阅 {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute：：RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ， [attribute：：DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md)， [catalog：：Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c)， [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md)， [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
