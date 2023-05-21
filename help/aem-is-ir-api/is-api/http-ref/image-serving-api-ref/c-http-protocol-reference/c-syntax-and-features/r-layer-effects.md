---
title: 圖層效果
description: Photoshop樣式圖層陰影和光暈效果是使用特殊子圖層（效果圖層）實作，這些子圖層可以附加到任何圖層（父圖層），包括layer=0和layer=comp。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 2%

---

# 圖層效果{#layer-effects}

Photoshop樣式圖層陰影和光暈效果是使用特殊子圖層（效果圖層）實作，這些子圖層可以附加到任何圖層（父圖層），包括layer=0和layer=comp。

雖然效果圖層支援許多標準的影像和圖層屬性及指令，但並非一般用途圖層，也不支援獨立的影像或文字資料。

任何數量的圖層效果都可以附加至單一父圖層。

## 內部和外部效果 {#section-2dade7ee98e041d1b4d1725e6f98a515}

*內部效果* 會呈現在上層圖層的頂端，而且只會在上層圖層的不透明區域顯示。 *外部效果* 會呈現在上層圖層後面（因此它們永遠無法在上層圖層的不透明區域中顯示），且可在合成畫布內的任何位置放置。 透過指定正或負的效果圖層編號來選擇內部或外部效果 `effect=` 命令。 此 `effect=` 指令也會控制附加至相同父圖層的多個效果圖層之間的z排序。

## 與上層圖層的關係 {#section-eb8bfc4f754a42fc973b562821d6f2d3}

效果圖層會自動調整大小並放置成與父圖層一致(亦即，效果圖層會繼承 `size=` 和 `origin=` 值)。 `pos=` 可用來將效果圖層從父圖層移開，這是下落和內陰影效果通常需要的功能。 而標準圖層則為 `pos=` 指定此圖層的起點與圖層0之間的位移，用於效果圖層 `pos=` 指定效果圖層的起點與父圖層之間的位移。

## 支援的命令和屬性 {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

效果圖層接受下列指令和屬性：

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

會忽略效果圖層中包含的所有其他影像和圖層指令。

## 預設效果巨集 {#section-a01e8dcc87c94495b54a6dfb21d2a718}

為方便圖層效果使用，IS提供兩個巨集與預設影像目錄， `$shadow$` 和 `$glow$`，可提供與Photoshop圖層效果類似的效果圖層屬性預設值。 下表列出應使用哪個效果指令和巨集來實作預設圖層效果。 自然地，可在URL中修改巨集中指定的任何屬性，或可建立其他巨集來實作自訂圖層效果。

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 所需效果</b> </th> 
   <th class="entry"> <b> 命令</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> 投影 </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 内阴影 </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 外发光 </p> </td> 
   <td> <p> <span class="codeph"> effect=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 内发光 </p> </td> 
   <td> <p> <span class="codeph"> effect=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-4c449fdf707b43858917fb271fa1fe96}

在圖層上增加三畫素寬、紅色邊框和50%的不透明度：

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

邊框將遵循影像的Alpha色版或遮色片的輪廓。 設定 `effect=1` 會將邊框放在內部邊緣上。

使用預設效果設定（顏色除外），在影像中新增藍色投影：

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` 在影像的右下邊緣增加一點邊界，可防止投影裁剪至影像邊界。

## 另请参阅 {#section-1acccccf534549aea23d4c008c17e7c0}

[effect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135)， [命令巨集%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
