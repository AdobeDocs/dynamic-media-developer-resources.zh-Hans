---
description: 最终的视图矩形。 允许将最终的视图图像拆分成若干条带或拼贴，这些条带或拼贴可以单独传送并由客户无缝地重新组装，而不会沿边缘产生任何伪影。
seo-description: 最终的视图矩形。 允许将最终的视图图像拆分成若干条带或拼贴，这些条带或拼贴可以单独传送并由客户无缝地重新组装，而不会沿边缘出现伪影。
seo-title: rect
solution: Experience Manager
title: rect
topic: Scene7 Image Serving - Image Rendering API
uuid: c4830fc5-d102-4789-8753-0a660d4a557e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# rect{#rect}

最终的视图矩形。 允许将最终的视图图像拆分成若干条带或拼贴，这些条带或拼贴可以单独传送并由客户无缝地重新组装，而不会沿边缘出现伪影。

`rect= *`坐`*, *``*[, *`标`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>在应用视图后，从视图图像左上角到矩形(int, int)左上角的像素偏移量（以像素表示） <span class="varname"></span> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 大小</span> </p></td> 
  <td class="stentry"> <p>ROI的大小（以像素为单位）(int、int)。 指定回复图像大小。 在视图图像未覆盖的区域中填充 <span class="codeph"> bgc=</span> (如果请求中存在fmt=*-alpha <span class="codeph"></span> ，则填充为左透明)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>缩放因子（实数）。 小于1.0的值会降低分辨率，大于1.0的值会增加分辨率。 </p></td> 
 </tr> 
</table>

使用此命令，图像服务可以通过HTTP传送大图像，否则，该图像将超出配置的大小限制 `attribute::MaxPix`。

>[!NOTE]
>
>为了在使用JPEG压缩时获得最佳效果，条带或拼贴大小应是JPEG编码拼贴大小（16x16像素）的倍数。

## 示例 {#section-932fcfcb41d74a29bc929e4430c49601}

将可打印的CMYK图像分成若干全分辨率条带，以减小下载文件的大小。 如果我们要请求连续图像：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

首先，获取图像的相关信息：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

文本响应包括以下属性：

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

根据这些信息，我们决定要四个600x2000像素条。 该命 `rect=` 令用于描述条带大小和位置。

由于此图像经常更改，我们将包含该命令，以尽可能减少从可能已在CDN或代理服务器中缓存的旧版本图像中找到一个或多个条带的可能性。 `id=` 属性的值 `image.version` 用于此目的。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## 属性 {#section-aae223cee13e46d38b74680c048d945b}

视图属性。 无论当前图层设置如何，均可应用。

扩展到视图图像之外的任何ROI区域都会用填充材料填充 `bgc=`。

最后 `rect=` 进行标定和配合 *、缩放、* 配合、 `scl=`配合等 `wid=``hei=``fit=``rgn=``align=`。

## 默认 {#section-b296d3bbfb19441f87137a452b70f19a}

整个未经修改的视图图像( `rect=0,0,width,height,1.0`)。

## 另请参阅 {#section-74015202c0c545ec82aec614d74b4bbd}

[裁剪=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) extend= [, wid=wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), scl= [, scl=scl,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)scl=pix align= [,fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)[lign=pix pix=Hei=Crop=Adrop=Adrop,Shapt属性：MaxMaxHei=id=i](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
