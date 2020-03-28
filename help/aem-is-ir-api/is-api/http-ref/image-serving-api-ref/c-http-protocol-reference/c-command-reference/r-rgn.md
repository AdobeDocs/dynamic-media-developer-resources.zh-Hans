---
description: 关注地区。 指定复合图像中的矩形感兴趣区域(ROI)，以像素表示。
seo-description: 关注地区。 指定复合图像中的矩形感兴趣区域(ROI)，以像素表示。
seo-title: rgn
solution: Experience Manager
title: rgn
topic: Scene7 Image Serving - Image Rendering API
uuid: 08657925-c52a-4279-8357-c26ad5c5ef3d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# rgn{#rgn}

关注地区。 指定复合图像中的矩形感兴趣区域(ROI)，以像素表示。

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>从复合图像的左上角到ROI的左上角的像素偏移量(int, int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 大小</span> </p></td> 
  <td class="stentry"> <p>ROI的大小（以像素为单位）(int、int)。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` 只定义ROI，而不裁切图像。 当 `wid=` 和／或大 `hei=` 于大于大小时，来自合成图像的附加数据在最终回复图像中可见。

## 属性 {#section-53edb35f4e364d7ca13fd0886e8b0c86}

视图属性。 无论当前图层设置如何，均可应用。

扩展到复合图像之外的任何ROI区域都会用填充 `bgc=`。

`rgn=` 在最终缩放和适合、、、 `scl=`、 `wid=``hei=`或之前应 `fit=`用 `rect=``align=`。

## 默认 {#section-6a3df8f670084def900ffef9dab7e94a}

整个复合图像( `rgn=0,0,width,height`)。

## 另请参阅 {#section-07883760f25c4d17aedbee36b7883891}

[裁剪=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) extend= [, wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), wid=hei= [, scl=,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)scl [=，对齐=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),fit=rect [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)[Hei=Rect](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
