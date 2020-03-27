---
description: Video360查看器的JavaScript API参考
seo-description: Video360查看器的JavaScript API参考
seo-title: setVideo
solution: Experience Manager
title: setVideo
topic: Dynamic media
uuid: 749aa32c-c27f-476c-954b-d4524528bccc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setVideo{#setvideo}

Video360查看器的JavaScript API参考

`setVideo(videoUrl)`

设置新的外部视频。 可以随时在修改前和修改后调用 `init()`。 如果在之后 `init()`调用，查看器将在运行时交换视频。

另请参阅 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## 参数 {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} ，指向新视频的绝对URL。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Viewers/space_station_360")
```

