---
description: Jpeg质量。 指定JPEG编码属性以控制压缩级别。 这反过来会改变文件大小（回复数据的数量），并间接改变生成图像的视觉质量。
seo-description: Jpeg质量。 指定JPEG编码属性以控制压缩级别。 这反过来会改变文件大小（回复数据的数量），并间接改变生成图像的视觉质量。
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 936607c1-20c3-4f76-b970-614b21c47dea
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 13%

---


# qlt{#qlt}

Jpeg质量。 指定JPEG编码属性以控制压缩级别。 这反过来会改变文件大小（回复数据的数量），并间接改变生成图像的视觉质量。

` qlt= *`质`*[, *`度`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 质量  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG编码质量(1...100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 色度  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度缩减采样(0=normal, 1=disable);可选，默认值为0。 </p> </td> 
 </tr> 
</table>

仅在`fmt=jpg`时使用。 忽略，否则

高品质值可增大文件并提升品质，低品质值可减小文件并降低可感知的图像品质。如果值大于 90，所产生的图像往往与未解压缩图像几乎没有区别。

设置`chroma`标志以禁用典型JPEG编码器采用的RGB色度缩减采样。 当边缘由色相而不是亮度的变化来定义时，这可能会增加图像中边缘的感知锐度。 设置此标志可能会使文件大小略有增加。 如果文本看起来略微模糊，则尝试使用此设置。

`chroma` 如果输出像素类型为CMYK或灰色，则忽略此值。

## 示例 {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
