---
description: 包括可选锁定后缀的请求字符串的整个修饰符部分的内容可以通过应用标准base64编码被遮住。
seo-description: 包括可选锁定后缀的请求字符串的整个修饰符部分的内容可以通过应用标准base64编码被遮住。
seo-title: 请求模糊处理
solution: Experience Manager
title: 请求模糊处理
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b12a78-c4ba-4b6d-97bc-63150298ed73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 请求模糊处理{#request-obfuscation}

包括可选锁定后缀的请求字符串的整个修饰符部分的内容可以通过应用标准base64编码被遮住。

如果设置了，服务器将尝试 `attribute::RequestObfuscation` 解码。 如果解码失败，则请求被拒绝。 如果同时应用了请求锁定和请求模糊处理，则必须在base64编码之前生成并附加锁定后缀。

## 示例 {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

编码为：

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

值字符串中“=”、“&amp;”和“%”的任何出现都必须使用“%xx”编码进行转义，然后才能模糊处理请求。 在模糊处理之前或之后，即使应用了请求锁定，也不必对请求的修饰符部分进行 *http编码* ，因为base64编码对于http传输是安全的。

## 另请参阅 {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP编码](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)，请 [求锁定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c)，属 [性：:RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
