---
title: qlt
description: Jpeg品质。 指定用于控制压缩级别的JPEG编码属性。 这反过来又会改变文件大小（回复数据的数量），并间接改变生成图像的视觉质量。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
TQID: 'https://experienceleague.adobe.com/sf3ydtf3lGCG1BfJfc1vW5hXFBawbeWJwXNSJdUEei8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 15%

---

# qlt{#qlt}

Jpeg品质。 指定用于控制压缩级别的JPEG编码属性。 这反过来又会改变文件大小（回复数据的数量），并间接改变生成图像的视觉质量。

` qlt= *`品质`*[, *`色度`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">品质</span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG编码质量(1...100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">色度</span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度降采样（0=正常，1=禁用）；可选，默认值为0。 </p> </td> 
 </tr> 
</table>

仅在`fmt=jpg`时使用。 已忽略，否则

高品质值可增大文件并提升品质，低品质值可减小文件并降低可感知的图像品质。 如果值大于 90，所产生的图像往往与未解压缩图像几乎没有区别。

设置`chroma`标志以禁用典型RGB编码器采用的JPEG色度缩减像素采样。 当边缘由色相变化而不是亮度变化来定义时，这可以增加图像中边缘的感知锐度。 设置此标志可能会导致文件大小略有增加。 如果文本看起来稍微模糊，请尝试使用此设置。

如果输出像素类型为CMYK或灰度，则忽略`chroma`。

## 示例 {#section-a6c263f15c29424a86ef267c96a6630a}

`http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80`
