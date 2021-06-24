---
description: Jpeg质量。 指定JPEG编码属性以控制压缩级别。 这进而会改变文件大小（回复数据的量），并间接地改变生成图像的视觉质量。
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 15%

---

# qlt{#qlt}

Jpeg质量。 指定JPEG编码属性以控制压缩级别。 这进而会改变文件大小（回复数据的量），并间接地改变生成图像的视觉质量。

` qlt= *``*[, *`质量色度`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 质量  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG编码质量(1...100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 色度  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度下采样(0=normal， 1=disable);可选，默认值为0。 </p> </td> 
 </tr> 
</table>

仅在`fmt=jpg`时使用。 否则忽略

高品质值可增大文件并提升品质，低品质值可减小文件并降低可感知的图像品质。如果值大于 90，所产生的图像往往与未解压缩图像几乎没有区别。

设置`chroma`标记以禁用典型JPEG编码器采用的RGB色度下采样。 当边缘由色相而不是亮度的变化来定义时，这可能会增加图像中边缘的感知锐度。 设置此标志可能会稍微增加文件大小。 如果文本看起来略微模糊，请尝试使用此设置。

`chroma` 如果输出像素类型为CMYK或灰色，则忽略此参数。

## 示例 {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
