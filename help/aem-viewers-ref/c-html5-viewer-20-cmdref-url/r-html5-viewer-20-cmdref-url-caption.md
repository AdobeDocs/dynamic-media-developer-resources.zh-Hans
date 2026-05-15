---
title: 题注
description: 所有查看者通用的参数。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
TQID: 'https://experienceleague.adobe.com/ydZxVPE4iwQMlJLnmCFXeAzkVX2cSGiuDzeNeEi5iaU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 5%

---

# 题注{#caption}

所有查看者通用的参数。

>[!NOTE]
>
>此命令不适用于视频图像查看器。

` caption= *`文件`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">文件</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT描述内容的URL或路径。 图像服务提供WebVTT文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 指定默认题注状态。 启用的是<span class="codeph"> 1 </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

此查看器支持通过托管的WebVTT文件使用隐藏式字幕。 使用此参数指定的字幕适用于媒体集中排名靠前的视频；后续播放的视频不含字幕。 不支持重叠提示和区域。 支持的提示定位运算符：

<table id="table_E752D7D8C1AA40C6B8A7057D2BB379C1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>鍵 </p> </th> 
   <th colname="col2" class="entry"> <p>名称 </p> </th> 
   <th colname="col3" class="entry"> <p>值 </p> </th> 
   <th colname="col4" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>测试对齐 </p> </td> 
   <td colname="col3"> <p> <span class="codeph">左|右|中|开始|结束</span> </p> </td> 
   <td colname="col4"> <p> 控制文本的对齐方式。 </p> <p>默认值为<span class="codeph">中间的</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>文本位置 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 注解文本开头插入VideoPlayer组件中的百分比。 </p> <p>默认值为<span class="codeph"> 0% </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>行大小 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 用于字幕的视频宽度的百分比。 </p> <p>默认值为<span class="codeph"> 100% </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>行位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整数 </p> </td> 
   <td colname="col4"> <p> 确定页面上的行位置。 </p> <p>如果以不带百分比符号的整数形式表示，则为文本显示位置上方的行数。 </p> <p>如果以百分比表示 — 百分比符号是最后一个字符 — 则说明文本在显示区域以百分比形式显示。 </p> <p>默认值为<span class="codeph"> 100% </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

如果WebVTT文件中存在任何其他WebVTT功能，则不支持这些功能；但是，它们不会中断字幕。

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">文件</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定URL或指向WebVTT描述内容的路径。 WebVTT文件由图像服务提供服务。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 指定默认题注状态。 </p> <p>启用的是<span class="codeph"> 1 </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-10ee45d637134e0fbcd943c62578cb78}

可选.

## 默认 {#section-d411e450028c460392cb8508f8ccc5d9}

无。

## 示例： {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
