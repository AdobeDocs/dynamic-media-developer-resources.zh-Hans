---
description: eCatalog Viewer的JavaScript API参考。
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic，查看器，SDK/API，电子目录搜索
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 2%

---


# setParam{#setparam}

eCatalog Viewer的JavaScript API参考。

[!DNL ` setParam( *`name， value`*)`]

将查看器参数设置为指定值。 该参数是特定于查看器的配置选项或软件开发工具包修饰符。 此参数在[!DNL `init()`]之前调用。

如果将查看器配置信息与[!DNL `config`] JSON对象一起传递给构造函数，则此方法是可选的。

另请参阅[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 名称  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}参 </span> 数的名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 值  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 参数值。该值不能以百分比编码。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
[!DNL <instance>.setParam("style", "customStyle.css")]
```

