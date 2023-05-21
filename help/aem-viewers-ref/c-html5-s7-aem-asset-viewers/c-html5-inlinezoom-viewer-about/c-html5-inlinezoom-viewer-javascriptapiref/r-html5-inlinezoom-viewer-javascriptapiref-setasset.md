---
title: setAsset
description: 內嵌縮放檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 62b46ad5-90b7-49e1-a426-87fbe956f07e
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---

# setAsset{#setasset}

內嵌縮放檢視器的JavaScript API參考。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 資產</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> 字串</span>} new asset id、explicit image set或explicit image set （含影格特定的Image Serving修飾元），後面附加了選用的全域Image Serving修飾元 <span class="codeph"> ？</span>. </p> <p> 此檢視器不支援使用IR （影像演算）或UGC （使用者產生的內容）的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定新資產。 您可以隨時在之前或之後呼叫此引數 `init()`. 如果是在之後呼叫 `init()`，檢視器會在執行階段交換資產。

另請參閱 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

單一影像參考：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

目錄中所定義影像集的單一參照：

```
<instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

明確影像集：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

使用影格特有的「影像伺服」修飾元設定明確的影像：

```
<instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

銳利化修飾元已新增至集中的所有影像：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```
