---
description: Jpeg大小（以千字节为单位）。 指定JPEG响应的最大大小（千字节）。
solution: Experience Manager
title: jpegSize
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 08cecb09-100f-4671-b335-d59c88b0e1ef
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---

# jpegSize{#jpegsize}

Jpeg大小（以千字节为单位）。 指定JPEG响应的最大大小（千字节）。

`jpegSize= *`大小`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 大小</span></span> </p> </td> 
  <td class="stentry"> <p>大小（千字节）。 </p></td> 
 </tr> 
</table>

如果将此值设置为正值，并且具有指定JPEG质量的JPEG响应未超过此值，则将返回该图像作为响应。 否则，JPEG质量会降低，直到它生成的图像符合指定的大小，或者直到它确定不适合为止。 在后一种情况下，请求失败，并出现错误。

值0表示响应不受大小约束。

不允许使用负值。

## 属性 {#section-19e544e77d35478b98fe8666f27d6968}

请求属性。 无论当前的层设置如何，都适用。 如果输出图像格式不是JPEG，则忽略此参数。

## 默认 {#section-198b798ed187453197e0969c641d6fb5}

0

## 示例 {#section-46bf806fd3ef4875b7726df32b6f834d}

确保大小不太大，无法传送到内存有限的设备：

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## 另请参阅 {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ，属 [性：:JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
