---
description: 响应多个req=类型而返回属性数据。
solution: Experience Manager
title: 属性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 748f68a1-f3ec-4249-a257-1115bcb3ee4c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 4%

---

# 属性{#properties}

属性数据是作为对以下内容的响应而返回的 `req=` 类型：

* `catalogprops`
* `imageprops`
* `props`
* `userdata`

`userdata` 仅当响应中包含以下内容时，才会将响应格式化为属性： `catalog::UserData` 遵循属性格式。

* [文本(Java)属性](r-text-java-properties.md)
* [JavaScript属性](r-javascript-properties.md)
* [XML属性](r-xml-properties.md)
* [JSONP属性](r-json-properties.md)


## 另请参阅 {#section-869fc97ffc4648f5a64062311be26819}

[req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
