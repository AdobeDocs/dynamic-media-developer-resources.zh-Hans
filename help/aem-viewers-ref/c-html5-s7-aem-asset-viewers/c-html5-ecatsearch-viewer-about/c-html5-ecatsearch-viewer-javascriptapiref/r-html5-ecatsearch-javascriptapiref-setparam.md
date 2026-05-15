---
description: eCatalog查看器的JavaScript API参考。
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0dd57c7e-c20f-4e8f-a872-42e24305fc0c
TQID: 'https://experienceleague.adobe.com/BVGAzU-4wHY2E61TO9IJZMc0b0DXwnYCsEtmDdIO0Wc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 2%

---

# setParam{#setparam}

eCatalog查看器的JavaScript API参考。

[!DNL ` setParam( *`名称，值`*)`]

将查看器参数设置为指定的值。 参数是特定于查看器的配置选项或软件开发工具包修饰符。 此参数在[!DNL `init()`]之前调用。

如果将查看器配置信息与[!DNL `config`] JSON对象一起传递给构造函数，则此方法是可选的。

另请参阅[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">名称</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span>参数名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">值</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span>参数值。 值不能采用百分比编码。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例： {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
[!DNL <instance>.setParam("style", "customStyle.css")]
```
