---
description: 通过应用标准base64编码，可以遮住请求字符串的整个修饰符部分的内容（包括可选的锁定后缀）。
seo-description: 通过应用标准base64编码，可以遮住请求字符串的整个修饰符部分的内容（包括可选的锁定后缀）。
seo-title: 请求模糊化
solution: Experience Manager
title: 请求模糊化
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b12a78-c4ba-4b6d-97bc-63150298ed73
translation-type: tm+mt
source-git-commit: 021c1d1f975083af3950775e230d4f73cbf9e0ec
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 1%

---


# 请求模糊化{#request-obfuscation}

通过应用标准base64编码，可以遮住请求字符串的整个修饰符部分的内容（包括可选的锁定后缀）。

如果设置了`attribute::RequestObfuscation`，服务器将尝试进行解码。 如果解码失败，则请求被拒绝。 如果同时应用了请求锁定和请求模糊处理，则必须在base64编码之前生成并附加锁后缀。

>[!IMPORTANT]
>
>如果启用此功能，请注意其使用存在以下某些限制：<br>-Dynamic Media用户界面可能无法显示&#x200B;**[!UICONTROL 上次发布时间]**&#x200B;字段的正确详细信息。 但是，此影响不会影响发布。<br>-当前，启用请求模糊处理和请&#x200B;**[!UICONTROL 求锁]** 定时， **[!UICONTROL HLS视]** 频流无法工作。<br>-目前，启用请求模糊处理和请求锁定 **[!UICONTROL 后，某]** 些Dynamic Media查 **[!UICONTROL 看]** 器将无法工作。

## 示例 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

编码为：

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

值字符串中“=”、“&amp;”和“%”的任何出现都必须使用“%xx”编码进行转义，然后才能对请求进行模糊处理。 在模糊化之前或之后，即使应用了请求锁定，也不必对请求的&#x200B;*修饰符*&#x200B;部分进行http编码，因为base64编码对http传输是安全的。

## 另请参阅 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP编码](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [请求锁定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c)，属 [性：:RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
