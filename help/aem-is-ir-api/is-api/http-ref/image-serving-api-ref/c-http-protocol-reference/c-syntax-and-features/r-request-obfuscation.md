---
description: 请求字符串的整个修饰符部分（包括可选锁定后缀）的内容可能会通过应用标准base64编码而被模糊。
solution: Experience Manager
title: 请求模糊处理
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---

# 请求模糊处理{#request-obfuscation}

请求字符串的整个修饰符部分（包括可选锁定后缀）的内容可能会通过应用标准base64编码而被模糊。

如果设置了`attribute::RequestObfuscation`，则服务器会尝试进行解码。 如果解码失败，则请求被拒绝。 如果同时应用了请求锁定和请求模糊处理，则必须在base64编码之前生成并附加锁定后缀。

>[!IMPORTANT]
>
>如果启用此功能，请注意，其使用存在某些限制，包括以下内容：<br> - Dynamic Media用户界面可能无法显示&#x200B;**[!UICONTROL 上次发布]**&#x200B;字段的正确详细信息。 但是，此影响不会影响发布。<br> — 目前，在启用请求模糊处理和请求锁定&#x200B;**[!UICONTROL 后，]** HLS视 **[!UICONTROL 频流]** 无法正常工作。<br> — 目前，在启用请求模糊处理和请求锁 **[!UICONTROL 定]** 后，某些Dynamic Media **[!UICONTROL 查看器]** 不起作用。

## 示例 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

编码为：

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

值字符串中出现“=”、“&amp;”和“%”的任何情况，都必须使用“%xx”编码进行转义，然后才能对请求进行模糊处理。 即使应用了请求锁定，也不必在模糊处理之前或之后对请求的&#x200B;*修饰符*&#x200B;部分进行http编码，因为base64编码对于http传输是安全的。

## 另请参阅 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP编码](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)、 [请求锁定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c)、 [属性：:RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
