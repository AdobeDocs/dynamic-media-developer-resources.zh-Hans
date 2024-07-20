---
title: setParam
description: 智能裁剪视频查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 193719b8-f158-4ffc-9916-b7b1bf36b2de
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 2%

---

# setParam{#setparam}

智能裁剪视频查看器的JavaScript API参考。

` setParam( *`名称，值`*)`

将查看器参数设置为指定的值。 参数是特定于查看器的配置选项或软件开发工具包修饰符。 此参数在`init()`之前调用。

如果将查看器配置信息与`config` JSON对象一起传递给构造函数，则此方法是可选的。

另请参阅[init](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

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

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
