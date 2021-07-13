---
description: 最终视图矩形。 允许将最终视图图像拆分成若干条或多块拼贴，这些拼贴可由客户无缝地单独传送和重新组装，而不会沿边缘出现伪影。
solution: Experience Manager
title: rect
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 1%

---

# rect{#rect}

最终视图矩形。 允许将最终视图图像拆分成若干条或多块拼贴，这些拼贴可以单独传送并由客户无缝地重新组装，而不会沿边缘出现伪影。

`rect= *``*, *``*[, *`坐标标尺`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>应用<span class="varname">缩放</span>后，从视图图像左上角到视图矩形(int， int)左上角的像素偏移（以像素表示）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 大小</span> </p></td> 
  <td class="stentry"> <p>ROI的大小(以像素为单位（整数、整数）。 指定回复图像大小。 在视图图像未覆盖的区域(或者，如果请求中存在<span class="codeph"> fmt=*-alpha</span>，则使用<span class="codeph"> bgc=</span>左透明)中填充图像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>比例因子（实数）。 小于1.0的值会降低分辨率，大于1.0的值会提高分辨率。 </p></td> 
 </tr> 
</table>

使用此命令，图像服务可以通过HTTP传送大图像，否则，该传送会超出使用`attribute::MaxPix`配置的大小限制。

>[!NOTE]
>
>为了在使用JPEG压缩时获得最佳结果，条带或拼贴大小应是JPEG编码拼贴大小（16x16像素）的倍数。

## 示例 {#section-932fcfcb41d74a29bc929e4430c49601}

将可打印的CMYK图像分割成若干全分辨率条带，以减小下载文件的大小。 如果我们要请求一个连续的图像：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

首先，获取图像的相关信息：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

文本响应包含以下属性：

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

根据这些信息，我们决定要四条600x2000像素条。 `rect=`命令用于描述条带大小和位置。

由于此图像经常更改，因此我们将使用`id=`命令来最大限度地减少最终出现该图像较旧版本（可能已缓存在CDN或代理服务器中）中一个或多个条带的可能性。 `image.version`属性的值用于此目的。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## 属性 {#section-aae223cee13e46d38b74680c048d945b}

查看属性。 无论当前的层设置如何，都适用。

扩展到视图图像以外的任何ROI区域都用`bgc=`填充。

在&#x200B;*、`wid=`、`hei=`、`fit=`、`rgn=`和`align=`的最终缩放和拟合后，应用重要的`rect=`。*`scl=`

## 默认 {#section-b296d3bbfb19441f87137a452b70f19a}

整个未修改的视图图像(`rect=0,0,width,height,1.0`)。

## 另请参阅 {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [属性：:MaxPix](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f),  [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5) [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
