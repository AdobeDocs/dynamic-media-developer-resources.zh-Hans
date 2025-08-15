---
title: 解析模式
description: 重新取样模式。 选择要用于缩放图像数据的重新取样和/或插值算法。 还适用于在视图转换期间文本图层的旋转和复合图像大小调整。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 1%

---

# 解析模式{#resmode}

重新取样模式。 选择要用于缩放图像数据的重新取样和/或插值算法。 还适用于在视图转换期间文本图层的旋转和复合图像大小调整。

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>选择标准的双线性插值。 最快速的重新取样方法；会出现一些锯齿伪像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>选择双三次插值。 CPU比双线性插值更加密集，但生成的图像更锐利，出现的锯齿伪像更少。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">锐化2 </span> </p> </td> 
   <td colname="col2"> <p>选择修改的Lanczos窗口函数作为插值算法。 能够以更高的CPU成本产生比双立方体更锐利的结果。 <span class="codeph"> sharp </span>已由<span class="codeph"> sharp2 </span>替换，这可能导致锯齿状工件(Moiré)的可能性较小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">两次锐化</span> </p> </td> 
   <td colname="col2"> <p>选择Photoshop默认重新取样器以减小图像大小，在Adobe Photoshop中称为“双三次锐化”。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>要在同时使用`resMode=bisharp`和`fit=stretch`时保持图像的宽高比，最佳做法是使用width参数或height参数。 如果必须定义这两个参数，则可以将它们封装在不同的图层中，如以下示例所示：
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## 属性 {#section-a171bacf4ddf43c782e46b86a16d443e}

请求属性。 适用于创建最终回复图像时涉及的所有缩放操作，包括所有图层缩放。

## 默认 {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## 示例 {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

检索存储在图像目录中的分层图像的最佳质量演绎版。 图像可以包含文本。 在图像编辑应用程序中进一步处理图像，从而请求图像的Alpha通道。

` http:// *`服务器`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## 另请参阅 {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute：：ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
