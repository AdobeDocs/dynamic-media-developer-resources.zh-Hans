---
title: setAsset
description: 混合媒體檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3ad78de9-17a6-40c9-b389-a1f7eed11635
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---

# setAsset{#setasset}

混合媒體檢視器的JavaScript API參考。

` setAsset( *`asset`*[,data]))`

設定新資產和選用的其他資產資料。 您可以隨時在之前或之後呼叫此引數 `init()`. 如果是在之後呼叫 `init()`，檢視器會在執行階段交換資產。

另請參閱 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## 参数 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`資產`*` - { `String`}新資產ID或明確混合媒體集，並於後面附加選用的影像伺服修飾元 `?`.

此檢視器不支援使用IR （影像演算）或UGC （使用者產生的內容）的影像。

`*`資料`*` - { `JSON`}新註解檔案的位置。

如果未指定，則不會在使用者介面中顯示註解按鈕。 使用此引數指定的註解會套用至混合媒體集中第一個出現的視訊；後續的視訊播放時不會加上註解。 此檢視器支援下列元件ID：

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>元件ID </p> </th> 
   <th colname="col2" class="entry"> <p>檢視器SDK元件類別名稱 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 後方影像 </span> </p> </td> 
   <td colname="col2"> <p>在視訊開始播放前第一個影格顯示的影像。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 註解 </span> </p> </td> 
   <td colname="col2"> <p> 新註解檔案的位置。 </p> <p>如果未指定，則不會在使用者介面中顯示註解按鈕。 以此引數指定的註解會套用至媒體集中排名第一的視訊。 後續影片播放時不會加上註解。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

單一媒體集參考：

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

明確媒體集：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

銳利化修飾元已新增至集中的所有影像：

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```
