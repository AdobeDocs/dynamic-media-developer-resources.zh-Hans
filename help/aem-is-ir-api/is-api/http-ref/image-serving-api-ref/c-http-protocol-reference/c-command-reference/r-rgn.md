---
title: rgn
description: 兴趣区域。 指定合成图像中的矩形感兴趣区域(ROI)，以像素表示。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fa597ba-f949-47f2-bb0f-5c078b5c7524
TQID: 'https://experienceleague.adobe.com/NJ--WHYqUvttsXg-Gn2-FyVUdZJG9SAduOLaaG80nY8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 2%

---

# rgn{#rgn}

兴趣区域。 指定合成图像中的矩形感兴趣区域(ROI)，以像素表示。

rgn= *`coord`*， *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">坐标</span> </p> </td> 
  <td class="stentry"> <p>从复合图像的左上角到ROI左上角的像素偏移(int， int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">大小</span> </p></td> 
  <td class="stentry"> <p>ROI的大小，以像素为单位(int， int)。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=`只定义ROI而不裁剪图像。 如果同时应用了大于大小的`wid=`和/或`hei=`，则复合图像中的其他数据可能会在最终回复图像中可见。

## 属性 {#section-53edb35f4e364d7ca13fd0886e8b0c86}

查看属性。 无论当前图层设置如何，均适用。

在复合图像之外扩展的ROI的任何区域都使用`bgc=`进行填充。

`rgn=`应用于`scl=`、`wid=`、`hei=`、`fit=`、`rect=`或`align=`的最终缩放和拟合之前。

## 默认 {#section-6a3df8f670084def900ffef9dab7e94a}

整个复合图像(`rgn=0,0,width,height`)。

## 另请参阅 {#section-07883760f25c4d17aedbee36b7883891}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ， [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)， [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)， [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)， [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)， [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)， [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)， [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
