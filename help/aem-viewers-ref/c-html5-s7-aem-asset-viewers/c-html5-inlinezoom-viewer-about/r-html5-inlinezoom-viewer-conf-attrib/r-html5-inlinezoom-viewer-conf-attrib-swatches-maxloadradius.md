---
title: 色板。最大加载半径
description: 色板。最大加载半径
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 574cb37c-009a-43c7-ae55-8b26c0c096c5
TQID: 'https://experienceleague.adobe.com/7o4IWCYXGbMgnqBW21NkOFl-6z4wuTR7cJSbAnRjNFU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 54
ht-degree: 5%

---

# 色板。最大加载半径{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> 指定组件预载行为。 当设置为<span class="codeph"> -1</span>时，在初始化组件或更改资产时，将同时加载所有样本。 当设置为<span class="codeph"> 0</span>时，将只加载可见的样本。 </p> <p><span class="codeph"> <span class="varname"> preloadnbr</span></span>定义可见区域周围预载多少不可见的行/列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选.

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`maxloadradius=-1`
