---
description: eCatalog查看器的JavaScript API参考。
solution: Experience Manager
title: setParams
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cbd7987b-5e47-4ac0-8235-a217e5e6dee9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 2%

---

# setParams{#setparams}

eCatalog查看器的JavaScript API参考。

[!DNL ` setParams( *`参数`*)`]

将一个或多个参数设置为给定值。 方法参数语法与URL查询字符串相同。 即，它表示用[!DNL `&`]分隔的名称=值对。 就像在查询字符串中一样，名称和值使用UTF8进行百分比编码。 调用[!DNL `init()`]之前，必须调用此参数。

如果将查看器配置信息与[!DNL `config`] JSON对象一起传递给构造函数，则此方法是可选的。

另请参阅[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">参数</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value参数对，以<span class="codeph"> &amp;</span>分隔。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("PageView.zoomstep=2,3&PageView.iscommand=op_sharpen%3d1")
```
