---
title: jpegSize
description: Jpeg大小（千字节）。 指定JPEG响应的最大大小（以KB为单位）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08cecb09-100f-4671-b335-d59c88b0e1ef
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# jpegSize{#jpegsize}

Jpeg大小（千字节）。 指定JPEG响应的最大大小（以KB为单位）。

`jpegSize= *`大小`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">大小</span></span> </p> </td> 
  <td class="stentry"> <p>大小(KB)。 </p></td> 
 </tr> 
</table>

如果将此值设置为正值，并且如果JPEG对指定JPEG质量的响应未超过此值，则该图像将作为响应返回。 否则，JPEG质量会降低，直到生成适合指定大小的图像或确定图像不适合为止。 在后一种情况下，请求会失败并出现错误。

值为0表示响应不受大小限制。

不允许负值。

## 属性 {#section-19e544e77d35478b98fe8666f27d6968}

请求属性。 无论当前图层设置如何，均适用。 如果输出图像格式不是JPEG，则忽略。

## 默认 {#section-198b798ed187453197e0969c641d6fb5}

0

## 示例 {#section-46bf806fd3ef4875b7726df32b6f834d}

保证的大小不会太大，无法传送到内存有限的设备：

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## 另请参阅 {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ，[attribute：：JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
