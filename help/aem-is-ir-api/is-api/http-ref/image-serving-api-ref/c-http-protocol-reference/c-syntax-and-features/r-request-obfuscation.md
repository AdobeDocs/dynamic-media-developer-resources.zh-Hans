---
description: 通过应用标准base64编码，可以遮蔽请求字符串的整个修饰符部分（包括可选锁后缀）的内容。
solution: Experience Manager
title: 请求模糊处理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---

# 请求模糊处理{#request-obfuscation}

通过应用标准base64编码，可以遮蔽请求字符串的整个修饰符部分（包括可选锁后缀）的内容。

服务器尝试在以下情况下进行解码： `attribute::RequestObfuscation` 设置。 如果解码失败，请求将被拒绝。 如果同时应用了请求锁定和请求模糊处理，则必须生成锁定后缀并在base64编码之前附加。

>[!IMPORTANT]
>
>如果启用此功能，请注意，其使用存在某些限制，包括：<br>-Dynamic Media用户界面可能不会显示针对的正确详细信息 **[!UICONTROL 上次发布时间]** 字段。 但是，此影响不会影响发布。<br> — 目前，HLS视频流在以下情况下不起作用： **[!UICONTROL 请求模糊处理]** 和 **[!UICONTROL 请求锁定]** 已启用。<br> — 目前，某些Dynamic Media查看器在以下情况下不起作用： **[!UICONTROL 请求模糊处理]** 和 **[!UICONTROL 请求锁定]** 已启用。

## 示例 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

编码为：

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

在对请求进行模糊处理之前，必须使用“%xx”编码对值字符串中出现的任何“=”、“&amp;”和“%”进行转义。 没有必要对 *修饰符* 混淆之前或之后的部分请求，即使应用了请求锁定也是如此，因为base64编码对http传输是安全的。

## 另请参阅 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP编码](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)， [请求锁定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c)， [attribute：：RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
