---
description: Video Viewer的JavaScript API參考。
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 5fd80f8d-321e-47f4-9fb2-65e7bd63be58
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---

# setAsset{#setasset}

Video Viewer的JavaScript API參考。

[!DNL ` setAsset( *`asset`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 資產 </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> 字串 </span>}新資產ID或明確影像集，且附加了選用的影像伺服修飾元 <span class="codeph"> ？ </span>. </p> <p> 此檢視器不支援使用IR （影像演算）或UGC （使用者產生的內容）的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定新資產。 您可以隨時在之前或之後呼叫此引數 [!DNL `init()`]. 如果是在之後呼叫 [!DNL `init()`]，檢視器會在執行階段交換資產。

另請參閱 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

目錄中所定義影像集的單一參照：

```
 <instance>.setAsset("Viewers/Pluralist")
```

明確的影像集，搭配預先組合的頁面：

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

明確的影像集，包含個別頁面影像：

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

銳利化修飾元已新增至集中的所有影像：

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```
