---
description: 利益区。 指定复合图像中的矩形感兴趣区域(ROI)，以像素表示。
solution: Experience Manager
title: rgn
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 3%

---


# rgn{#rgn}

利益区。 指定复合图像中的矩形感兴趣区域(ROI)，以像素表示。

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>从复合图像左上角到ROI左上角(int， int)的像素偏移。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 大小</span> </p></td> 
  <td class="stentry"> <p>ROI的大小(以像素为单位(int， int))。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` 只定义ROI，而不裁切图像。当`wid=`和/或`hei=`大于大于大小时，来自合成图像的附加数据可以在最终回复图像中可见。

## 属性 {#section-53edb35f4e364d7ca13fd0886e8b0c86}

视图属性。 无论当前图层设置如何，均适用。

扩展到复合图像以外的ROI的任何区域都用`bgc=`填充。

`rgn=` 在最终缩放和拟合之前应 `scl=`用 `wid=`、 `hei=`、 `fit=` `rect=`、 `align=`或。

## 默认 {#section-6a3df8f670084def900ffef9dab7e94a}

整个复合图像(`rgn=0,0,width,height`)。

## 另请参阅 {#section-07883760f25c4d17aedbee36b7883891}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [延伸=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), wid= [, wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)hei= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)scl=,  [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989) [=, fit=, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
