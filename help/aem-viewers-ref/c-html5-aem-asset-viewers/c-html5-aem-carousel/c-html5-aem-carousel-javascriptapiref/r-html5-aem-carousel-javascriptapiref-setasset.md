---
title: setAsset
description: 轉盤檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: e8aaee4e-56d5-46e4-8499-d5c9a6ba5d3b
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---

# setAsset{#setasset}

轉盤檢視器的JavaScript API參考。

` setAsset( *`asset`*)`

設定新資產。 您可以隨時在之前或之後呼叫此引數 `init()`. 如果是在之後呼叫 `init()`，檢視器會在執行階段交換資產。

另請參閱 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 資產</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> 字串</span>}個新資產ID。 </p> <p>此檢視器不支援使用IR （影像演算）或UGC （使用者產生的內容）的影像。 </p> </td>
  </tr>
 </tbody>
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

單一影像參考：

```
<instance>.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner")
```

