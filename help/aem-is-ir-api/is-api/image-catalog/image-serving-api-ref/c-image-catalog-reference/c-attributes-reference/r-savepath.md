---
description: saveToFile=的根路径。 应将使用req=saveToFile生成的图像写入到的根文件夹的相对路径。
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---


# SavePath{#savepath}

saveToFile=的根路径。 应将使用req=saveToFile生成的图像写入到的根文件夹的相对路径。

`SavePath` 是文本字符串值。

## 属性 {#section-343d1371e966491c92854a8df14c3c50}

文本字符串。 必须为空或有效的相对文件夹路径。 始终与使用`ImageServer::SaveDirectory`配置的绝对根路径组合。

## 默认 {#section-ae751eea97654f399c6aaee3f3252cbb}

如果未定义，则从`default::SavePath`继承。 如果解析的值为空，则禁用保存到文件。

## 另请参阅 {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
