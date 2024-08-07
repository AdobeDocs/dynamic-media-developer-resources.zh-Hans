---
title: asset
description: 所有查看者通用的参数。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: edcd18b6-5292-44da-80be-b7f75ee4c48e
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 2%

---

# asset{#asset}

所有查看者通用的参数。

` asset= *`资产ID`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">资产ID </span> </span> </p> </td> 
   <td colname="col2"> <p> 单个视频或自适应视频集的资产ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

除非使用`video`参数，否则需要此属性。 请参阅视频下的[外部视频支持](../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3)或视频360下的[外部视频支持](../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760)。

或者

` asset= *`图像`*`

<table id="table_67E18F42E97C4AAAB0A2F67B7924765D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">图像</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定单个图像或轮播集。 将双重HTTP编码应用于图像名称或轮播集名称中存在的任何不安全字符。 </p> </td> 
  </tr> 
 </tbody> 
</table>

或者

` asset= *`image`* | *`imageList`* | *`imageListWithModifiers`* | *`multiDimensionalSpinSet`* [%3F *`修饰符`*]`

<table id="table_A2A0ACD942E942BC99AF0DC80FB1C670"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">图像</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定单个图像。 将双重HTTP编码应用于映像名称中存在的任何不安全字符。 </p> <p>或者，指定对图像集的引用。 查看器使用<span class="codeph"> req=set IS </span>请求从服务器检索图像集。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">图像列表</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定显式图像集，它由以逗号分隔的已排序项目或帧序列组成。 </p> <p> <p>注意：此功能在Adobe Dynamic Media Classic中受支持；在Adobe Experience Manager Assets中不受支持。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageListWithModifiers </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定一个显式图像集，其中每个帧都有自己的图像服务修饰符。 在这种情况下，框架列表将包含在括号中。 确保将双HTTP编码应用于帧特定的图像服务修饰符中存在的任意逗号。 </p> <p> <p>注意：此功能在Adobe Dynamic Media Classic中受支持；在Adobe Experience Manager Assets中不受支持。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> multiDimensionalSpinSet </span> </span> </p> </td> 
   <td colname="col2"> <p>使用以下语法指定显式多维旋转集： </p> <p> <span class="codeph"> (（<span class="varname">水平旋转集</span>）[，（<span class="varname">水平旋转集</span>）]) </span> </p> <p> 其中<span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span>是给定水平轴的逗号分隔框架列表。 所有<span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span>应具有相同的帧数。 </p> <p> <p>注意：此功能在Adobe Dynamic Media Classic中受支持；在Adobe Experience Manager Assets中不受支持。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">修饰符</span> </span> </p> </td> 
   <td colname="col2"> <p> 图像服务命令；<span class="codeph"> &amp; </span>和<span class="codeph"> = </span>分隔符必须通过HTTP编码分别表示为<span class="codeph"> %26 </span>和<span class="codeph"> %3D </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

或者

` asset=( *`mediaSet`* | ( *`视频`*; *`swatchId`* | *`图像`*; *`swatchId`* | *`setId`*; *`swatchId`*); *`ID`*;( *`视频`*; *`swatchId`* | *`图像`*; *`swatchId`* | *`setId`*; *`swatchId`*); *`ID`*;] [%3F *`修饰符`*]`

<table id="table_D31C8507C02A4452A79DEDDEC62EF2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">媒体集</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定对媒体集的引用。 查看器使用req=set IS请求从服务器检索媒体集。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">视频</span> </span> </p> </td> 
   <td colname="col2"> <p> 单个视频或自适应视频集。 </p> <p> <p>注意：此功能在Adobe Dynamic Media Classic中受支持；在Adobe Experience Manager Assets中不受支持。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">图像</span> </span> </p> </td> 
   <td colname="col2"> <p> 单个图像。 </p> <p> <p>注意：此功能在Adobe Dynamic Media Classic中受支持；在Adobe Experience Manager Assets中不受支持。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> setId </span> </span> </p> </td> 
   <td colname="col2"> <p> 样本集。 </p> <p> <p>注意：此功能在Adobe Dynamic Media Classic中受支持；在Adobe Experience Manager Assets中不受支持。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> swatchId </span> </span> </p> </td> 
   <td colname="col2"> <p>样本图像。 </p> <p> <p>注意：此功能在Adobe Dynamic Media Classic中受支持；在Adobe Experience Manager Assets中不受支持。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID </span> </span> </p> </td> 
   <td colname="col2"> <p> 媒体集项目类型标识符可以是以下任一项： </p> <p> 
     <ul id="ul_3100F9356628498DA820C07F6F69CC9B"> 
      <li id="li_51B649A539F14510873CFDA85A6AA714"> <p> <span class="codeph"> advanced_image </span> </p> <p>用于单个图像。 </p> </li> 
      <li id="li_7E764D67294647C1A828F949E5ED1908"> <p> <span class="codeph"> advanced_swatchset </span> </p> <p>对于嵌套样本集。 </p> </li> 
      <li id="li_C942CED779B54110BCDC74188995FD5B"> <p> <span class="codeph">旋转</span> </p> <p>用于旋转集。 </p> </li> 
      <li id="li_6EA5C54F078D4B24B44F1588BF083842"> <p> <span class="codeph">视频</span> </p> <p>用于单个视频。 </p> </li> 
      <li id="li_8110FA7E0CAB4681A2D8C15F2A656E69"> <p> <span class="codeph">视频集</span> </p> <p>用于自适应视频集。 </p> </li> 
     </ul> </p> <p> <p>注意：此功能在Adobe Dynamic Media Classic中受支持；在Adobe Experience Manager Assets中不受支持。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">修饰符</span> </span> </p> </td> 
   <td colname="col2"> <p> 图像服务命令；<span class="codeph"> &amp; </span>和<span class="codeph"> = </span>分隔符必须通过HTTP编码分别表示为<span class="codeph"> %26 </span>和<span class="codeph"> %3D </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。

## 属性 {#section-10ee45d637134e0fbcd943c62578cb78}

必需.

## 默认 {#section-d411e450028c460392cb8508f8ccc5d9}

无。

## 示例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

单个资源引用：

```
asset=Scene7SharedAssets/Backpack_B
```

或者

```
asset=/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg
```

或者

```
asset=/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4
```

或者

```
asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner
```

或者

```
asset=Viewers/space_station_360-AVS
```

对目录中定义的图像集的单个引用：

```
asset=Viewers/Pluralist
```

显式图像集：

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C
```

使用特定于帧的图像服务修饰符的显式图像集：

```
asset=(Scene7SharedAssets/Backpack_B%3Fop_colorize%3D255%252C0%252C0,Scene7SharedAssets/Backpack_B%3Fop_colorize%3D0x00ff00)
```

对目录中定义的旋转集的单个引用：

```
asset=Scene7SharedAssets/SpinSet-Sample
```

显式旋转集：

```
asset=Scene7SharedAssets/Frame-1,Scene7SharedAssets/Frame-2,Scene7SharedAssets/Frame-3,Scene7SharedAssets/Frame-4,Scene7SharedAssets/Frame-5,Scene7SharedAssets/Frame-6,Scene7SharedAssets/Frame-7,Scene7SharedAssets/Frame-8
```

显式多维旋转集：

```
asset=((Scene7SharedAssets/ring1-25,Scene7SharedAssets/ring1-26,Scene7SharedAssets/ring1-27,Scene7SharedAssets/ring1-28,Scene7SharedAssets/ring1-29,Scene7SharedAssets/ring1-30,Scene7SharedAssets/ring1-31,Scene7SharedAssets/ring1-32,Scene7SharedAssets/ring1-33,Scene7SharedAssets/ring1-34,Scene7SharedAssets/ring1-35,Scene7SharedAssets/ring1-36),(Scene7SharedAssets/ring1-13,Scene7SharedAssets/ring1-14,Scene7SharedAssets/ring1-15,Scene7SharedAssets/ring1-16,Scene7SharedAssets/ring1-17,Scene7SharedAssets/ring1-18,Scene7SharedAssets/ring1-19,Scene7SharedAssets/ring1-20,Scene7SharedAssets/ring1-21,Scene7SharedAssets/ring1-22,Scene7SharedAssets/ring1-23,Scene7SharedAssets/ring1-24),(Scene7SharedAssets/ring1-01,Scene7SharedAssets/ring1-02,Scene7SharedAssets/ring1-03,Scene7SharedAssets/ring1-04,Scene7SharedAssets/ring1-05,Scene7SharedAssets/ring1-06,Scene7SharedAssets/ring1-07,Scene7SharedAssets/ring1-08,Scene7SharedAssets/ring1-09,Scene7SharedAssets/ring1-10,Scene7SharedAssets/ring1-11,Scene7SharedAssets/ring1-12))
```

单个混合媒体集引用：

```
 asset=Scene7SharedAssets/Mixed_Media_Set_Sample
```

显式混合媒体集：

```
asset=Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;
```

向集中的所有图像添加了锐化修饰符：

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C%3Fop_sharpen=%3D1
```

```
asset=Scene7SharedAssets/Mixed_Media_Set_Sample%3Fop_sharpen%3D1
```

```
asset=Viewers/Pluralist%3Fop_sharpen%3D1
```
