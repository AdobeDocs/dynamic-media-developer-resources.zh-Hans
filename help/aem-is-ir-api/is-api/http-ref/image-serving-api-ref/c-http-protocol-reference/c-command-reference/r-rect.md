---
description: 最终视图矩形。 允许将最终视图图像分解成若干条或拼贴，这些条或拼贴可以单独传送并由客户无缝地重新组合，而不会沿边缘产生伪影。
seo-description: 最终视图矩形。 允许将最终视图图像分解成若干条或拼贴，这些条或拼贴可以单独传送并由客户无缝地重新组合，而不会沿边缘产生伪影。
seo-title: rect
solution: Experience Manager
title: rect
topic: Scene7 Image Serving - Image Rendering API
uuid: c4830fc5-d102-4789-8753-0a660d4a557e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---


# rect{#rect}

最终视图矩形。 允许将最终视图图像分解成若干条或拼贴，这些条或拼贴可以单独传送并由客户无缝地重新组合，而不会沿边缘产生伪影。

`rect= *``*, *``*[, *`坐标`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐标</span> </p> </td> 
  <td class="stentry"> <p>应用<span class="varname">缩放</span>后，从视图图像的左上角到视图矩形(int, int)的左上角的像素偏移量（以像素表示）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 大小</span> </p></td> 
  <td class="stentry"> <p>ROI的大小（以像素为单位）(int、int)。 指定回复图像大小。 在视图图像未覆盖的区域中，用<span class="codeph"> bgc=</span>填充图像（如果请求中存在<span class="codeph"> fmt=*-alpha</span>，则用左透明填充）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>缩放因子（实数）。 小于1.0的值会降低分辨率，大于1.0的值会提高分辨率。 </p></td> 
 </tr> 
</table>

使用此命令，图像服务可以通过HTTP传送大图像，否则，该传送将超过使用`attribute::MaxPix`配置的大小限制。

>[!NOTE]
>
>为在使用JPEG压缩时获得最佳效果，条带或拼贴大小应是JPEG编码拼贴大小（16x16像素）的倍数。

## 示例 {#section-932fcfcb41d74a29bc929e4430c49601}

将可打印的CMYK图像分为几个全分辨率条带，以减小下载文件的大小。 如果要请求连续图像：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

首先，获取图像的相关信息：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

文本响应包括以下属性：

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

根据这些信息，我们决定要4条600x2000像素的条带。 `rect=`命令用于描述条带大小和位置。

由于此图像经常更改，因此我们将使用`id=`命令来尽可能减少从图像的较旧版本（可能已在CDN或代理服务器中缓存）中找到一个或多个条带的可能性。 `image.version`属性的值用于此用途。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## 属性 {#section-aae223cee13e46d38b74680c048d945b}

视图属性。 无论当前图层设置如何，均适用。

扩展到视图图像以外的ROI的任何区域都用`bgc=`填充。

重要`rect=`在&#x200B;*、`wid=`、`hei=`、`fit=`、`rgn=`和`align=`之后应用*。`scl=`

## 默认 {#section-b296d3bbfb19441f87137a452b70f19a}

完整、未修改的视图图像(`rect=0,0,width,height,1.0`)。

## 另请参阅 {#section-74015202c0c545ec82aec614d74b4bbd}

[裁切=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ，延伸= [, wid=hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [schi=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [sc=, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5) [,=,=,=，属性：: MaxMaxHid, id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
