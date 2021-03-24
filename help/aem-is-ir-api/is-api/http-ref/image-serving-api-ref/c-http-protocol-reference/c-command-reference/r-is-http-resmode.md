---
description: 重新取样模式。 选择用于缩放图像数据的重新取样和/或插值算法。 还适用于在视图变换期间旋转文本图层和调整复合图像大小。
solution: Experience Manager
title: resMode
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 12%

---


# resMode{#resmode}

重新取样模式。 选择用于缩放图像数据的重新取样和/或插值算法。 还适用于在视图变换期间旋转文本图层和调整复合图像大小。

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 比林  </span> </p> </td> 
   <td colname="col2"> <p>选择标准双线性插值。 最快的重新取样方法；某些锯齿伪影会相当明显。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 比库  </span> </p> </td> 
   <td colname="col2"> <p>选择双三次插值。 与双线性插值相比，CPU占用更多，但会生成较锐利的图像，出现的锯齿伪像较少。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>选择一个修改的Lanczos窗口函数作为插值算法。 相对于双三次插值法，产生的结果可能是锐度更高，但 CPU 占用更多。<span class="codeph"> sharp已 </span> 被sharp2所替 <span class="codeph"> 换， </span>它导致锯齿伪像(Moiré)的可能性较小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 比沙尔  </span> </p> </td> 
   <td colname="col2"> <p>选择Photoshop默认重新取样器以减小图像大小，在Adobe Photoshop中称为“双立方（锐化）”。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-a171bacf4ddf43c782e46b86a16d443e}

请求属性。 适用于创建最终回复图像时涉及的所有缩放操作，包括所有图层缩放。

## 默认 {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## 示例 {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

检索存储在图像目录中的分层图像的最佳质量再现。 图像可能包含文本。 我们期望在图像编辑应用程序中进行进一步处理，从而请求对图像进行Alpha渠道。

` http:// *`伺服器`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## 另请参阅 {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[属性：:ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
