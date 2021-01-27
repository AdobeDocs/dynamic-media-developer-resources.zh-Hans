---
description: Video360查看器的JavaScript API参考
seo-description: Video360查看器的JavaScript API参考
seo-title: setVideo
solution: Experience Manager
title: setVideo
topic: Dynamic Media
uuid: 749aa32c-c27f-476c-954b-d4524528bccc
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 4%

---


# setVideo{#setvideo}

Video360查看器的JavaScript API参考

`setVideo(videoUrl)`

设置新的外部视频。 可以随时在`init()`前后调用。 如果在`init()`之后调用，则查看器在运行时交换视频。

另请参阅[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## 参数 {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl  </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph">字符串</span>}是指向新视频的绝对URL。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Viewers/space_station_360")
```

