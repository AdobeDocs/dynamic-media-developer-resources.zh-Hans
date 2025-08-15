---
description: 响应图像格式。
solution: Experience Manager
title: 格式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e179fc51-0461-4000-99eb-4390c35d5606
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 3%

---

# 格式{#fmt}

响应图像格式。

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">格式</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif-alpha | swf | pdf | gif | gif-alpha | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> 指定发送到客户端的图像数据的图像编码格式以及HTTP回复标头的相应响应MIME类型。 </p> <p> <span class="codeph"> jpeg </span>：有损JPEG </p> <p> <span class="codeph"> png </span>：无损失PNG </p> <p> <span class="codeph"> png-alpha </span>：带有alpha通道的无损PNG </p> <p> <span class="codeph"> tif </span>： TIFF </p> <p> <span class="codeph"> tif-alpha </span>：带有alpha通道的TIFF </p> <p> <span class="codeph"> swf </span>：嵌入到Adobe swf文件中的有损JPEG </p> <p> <span class="codeph"> pdf </span>：图像嵌入到PDF中 </p> <p> <span class="codeph"> gif </span>： GIF具有2到256色 </p> <p> <span class="codeph"> gif-alpha </span>：GIF，具有2到255色加上键色透明度 </p> <p> <span class="codeph"> fxg </span>：应用了变量和DOM操作的FXG </p> <p> <span class="codeph"> fxgraw </span>：原始FXG存储在服务器上 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb | 灰色 | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> 可用于影响输出颜色空间。 </p> <p> <span class="codeph"> rgb </span>：返回RGB图像数据 </p> <p> <span class="codeph">灰度</span>：返回灰度图像数据 </p> <p> <span class="codeph"> cmyk </span>：返回CMYK图像数据 </p> </td> 
 </tr> 
</table>

仅当指定tif、tif-alpha作为格式时，才允许`tiffCompression`。 有关这些图像格式支持的压缩选项，请参阅下表。

`qlt=`可用于为以下格式设置JPEG编码选项：JPEG、带有JPEG压缩的TIFF。 如果fmt=gif或fmt=gif-alpha，可以使用quantize=。 有关详细信息，请参阅命令说明。 其他格式没有可设置的选项。

对于所有格式和`pixelTypes[7]`，每像素组件返回8位。

下表列出了格式和`pixelType`的有效组合，以及相应的HTTP响应MIME类型。

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname">格式</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>响应MIME类型 </p> </th> 
   <th colname="col4" class="entry"> <p>嵌入ICC配置文件 </p> </th> 
   <th colname="col5" class="entry"> <p>选项 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb、灰度、cmyk </p> </td> 
   <td> <p>&lt;image/jpeg&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png， png-alpha </p> </td> 
   <td> <p>rgb，灰度 </p> </td> 
   <td> <p>&lt;image/png&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif， tif-alpha </p> </td> 
   <td> <p>rgb、灰度、cmyk </p> </td> 
   <td> <p>&lt;image/tiff&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> (无 | lzw | zip | jpeg)，qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf， swf-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application/x-shockwave-flash&gt; </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p><span class="codeph"> qlt= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rgb、灰度、cmyk </p> </td> 
   <td> <p>&lt;application/pdf&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif， gif-alpha </p> </td> 
   <td> <p>rgb，灰度 </p> </td> 
   <td> <p>&lt;image/gif&gt; </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p><span class="codeph">量化=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
