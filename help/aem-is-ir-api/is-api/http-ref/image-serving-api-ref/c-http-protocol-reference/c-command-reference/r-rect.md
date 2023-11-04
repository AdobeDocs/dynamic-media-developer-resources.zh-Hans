---
title: 矩形
description: 最终视图矩形。 它允许将最终视图图像拆分为若干条或拼贴，这些条或拼贴可以单独交付并由客户端无缝重组，边缘没有伪像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 1%

---

# 矩形{#rect}

最终视图矩形。 它允许将最终视图图像拆分为若干条或拼贴，这些条或拼贴可以单独交付并由客户端无缝重组，边缘没有伪像。

`rect= *`坐标`*, *`大小`*[, *`缩放`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐标</span> </p> </td> 
  <td class="stentry"> <p>从视图图像的左上角到视图矩形(int， int)左上角的像素偏移，以像素表示，在如下位置之后 <span class="varname"> 缩放</span> 中所有规则都适用的URL的区域。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 大小</span> </p></td> 
  <td class="stentry"> <p>ROI的大小，以像素为单位(int， int)。 指定回复图像大小。 图像填充了 <span class="codeph"> bgc=</span> 在视图图像未覆盖的区域中(或保持透明，如果 <span class="codeph"> fmt=*-alpha</span> 存在于请求中)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>缩放因子（实际）。 小于1.0的值会降低分辨率，大于1.0的值会提高分辨率。 </p></td> 
 </tr> 
</table>

使用此命令，图像服务可以通过HTTP交付大图像，否则将超过配置的大小限制。 `attribute::MaxPix`.

>[!NOTE]
>
>为获得最佳结果，当使用JPEG压缩时，条带或拼贴大小应为JPEG编码拼贴大小（16x16像素）的倍数。

## 示例 {#section-932fcfcb41d74a29bc929e4430c49601}

将可打印的CMYK图像分成几个全分辨率条带以减小下载文件的大小。 如果您请求了连续的图像：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

首先，获取图像的相关信息：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

文本响应包括以下属性：

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

根据此信息，需要四条600x2000像素的条带。 此 `rect=` 命令用于描述条带的大小和位置。

由于此图像经常更改，因此 `id=` 命令包括在内。 这样做可以最大限度地减少旧版本中可能已缓存到CDN或代理服务器中的一个或多个图像条出现的机会。 的值 `image.version` 属性用于此目的。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## 属性 {#section-aae223cee13e46d38b74680c048d945b}

查看属性。 无论当前图层设置如何，它都适用。

在视图图像之外扩展的ROI的任何区域都填充了 `bgc=`.

重要 `rect=` 已应用 *之后* 最终缩放和拟合 `scl=`， `wid=`， `hei=`， `fit=`， `rgn=`、和 `align=`.

## 默认 {#section-b296d3bbfb19441f87137a452b70f19a}

完整、未修改的视图图像( `rect=0,0,width,height,1.0`)。

## 另请参阅 {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ， [扩展=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)， [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)， [嘻=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)， [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)， [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)， [适合=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)， [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)， [attribute：：MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)， [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
