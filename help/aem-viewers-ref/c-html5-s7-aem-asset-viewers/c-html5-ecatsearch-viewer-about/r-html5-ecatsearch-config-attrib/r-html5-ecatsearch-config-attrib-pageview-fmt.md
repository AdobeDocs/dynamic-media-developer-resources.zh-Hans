---
description: PageView.fmt
solution: Experience Manager
title: PageView.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 690aed79-c242-402d-86c0-470a91fbb034
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# PageView.fmt{#pageview-fmt}

[!DNL `[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定元件從影像伺服器載入影像時所用的影像格式。 如果指定的格式結尾為 <span class="codeph"> -alpha</span>，元件會將影像呈現為透明內容。 對於所有其他影像格式，元件會將影像視為不透明。 元件預設為白色背景。 因此，若要使其透明，請設定 <span class="codeph"> background-color</span> CSS屬性至 <span class="codeph"> 透明</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-12a6fb2fcbc1476b95bd53ce880dc185}

可选.

## 默认 {#section-4b6a350501124ffa9a6b1b71b32eff5d}

[!DNL `jpeg`]

## 示例 {#section-7de29e43bb3640e4aa1f8984b4afddad}

[!DNL `fmt=png-alpha`]
