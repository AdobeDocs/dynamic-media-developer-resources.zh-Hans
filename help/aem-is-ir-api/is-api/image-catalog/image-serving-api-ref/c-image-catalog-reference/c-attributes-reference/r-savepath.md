---
description: saveToFile=的根路径。 根文件夹的相对路径，应将通过req=saveToFile生成的图像写入到该根文件夹。
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 6e2814b9-898f-4cf4-8e4f-aa972d554213
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---

# SavePath{#savepath}

saveToFile=的根路径。 根文件夹的相对路径，应将通过req=saveToFile生成的图像写入到该根文件夹。

`SavePath` 是文本字符串值。

## 属性 {#section-343d1371e966491c92854a8df14c3c50}

文本字符串。 必须为空或有效的相对文件夹路径。 始终与配置了`ImageServer::SaveDirectory`的绝对根路径组合。

## 默认 {#section-ae751eea97654f399c6aaee3f3252cbb}

从`default::SavePath`继承（如果未定义）。 如果解析的值为空，则禁用“保存到文件”。

## 另请参阅 {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
