---
description: 响应图像格式。
seo-description: 响应图像格式。
seo-title: fmt
solution: Experience Manager
title: fmt
uuid: 78ee7545-5ad9-4240-bbfc-20efe3e42ed3
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 3%

---


# fmt{#fmt}

响应图像格式。

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 格式</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif-alpha | swf | pdf | gif | gif-alpha | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> 为发送到客户端的图像数据指定图像编码格式，为HTTP回复标头指定相应的响应MIME类型。 </p> <p> <span class="codeph">  jpeg  </span>:有损JPEG </p> <p> <span class="codeph"> png  </span>:无丢失PNG </p> <p> <span class="codeph"> png-alpha  </span>:带有alpha渠道的无丢失PNG </p> <p> <span class="codeph">  tif  </span>:TIFF </p> <p> <span class="codeph"> tif-alpha  </span>:带有Alpha渠道的TIFF </p> <p> <span class="codeph">  swf  </span>:嵌入到Adobeswf文件中的有损JPEG </p> <p> <span class="codeph"> pdf  </span>:嵌入PDF中的图像 </p> <p> <span class="codeph"> gif  </span>:2到256色的GIF </p> <p> <span class="codeph"> gif-alpha  </span>:具有2到255种颜色加上主色透明度的GIF </p> <p> <span class="codeph"> fxg  </span>:应用了变量和DOM操作的FXG </p> <p> <span class="codeph">  fxgraw  </span>:存储在服务器上的原始FXG </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rg |灰色 | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> 可用于影响输出色彩空间。 </p> <p> <span class="codeph">  rgb  </span>:返回RGB图像数据 </p> <p> <span class="codeph"> 灰色 </span>:返回灰度图像数据 </p> <p> <span class="codeph"> cmyk  </span>:返回CMYK图像数据 </p> </td> 
 </tr> 
</table>

`tiffCompression` 仅当将tif-alpha指定为格式时才允许。有关这些图像格式支持的压缩选项，请参阅下表。

`qlt=` 可用于为以下格式设置JPEG编码选项：JPEG、TIFF（带JPEG压缩）。如果fmt=gif或fmt=gif-alpha，则可以使用quantize=。 有关详细信息，请参阅命令说明。 其他格式没有可设置的选项。

为所有格式和`pixelTypes[7]`返回每像素8位组件。

下表列表了格式和`pixelType`（相应的HTTP响应MIME类型）的有效组合。

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> 格式</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>响应MIME类型 </p> </th> 
   <th colname="col4" class="entry"> <p>嵌入ICC用户档案 </p> </th> 
   <th colname="col5" class="entry"> <p>选项 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb，灰色，cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png、png-alpha </p> </td> 
   <td> <p>rgb，灰色 </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif， tif-alpha </p> </td> 
   <td> <p>rgb，灰色，cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> (none | lzw | zip | jpeg)、qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf，swf-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p><span class="codeph"> qlt=  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rgb，灰色，cmyk </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif，gif-alpha </p> </td> 
   <td> <p>rgb，灰色 </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p><span class="codeph"> 数量=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
