---
title: setParam
description: 全景查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 2%

---

# setParam{#setparam}

全景查看器的JavaScript API参考。

` setParam( *`名称，值`*)`

将查看器参数设置为指定的值。 参数是查看器特定的配置选项或软件开发工具包修饰符。 此参数是在之前调用的 `init()`.

如果通过以下方式传递查看器配置信息，则可以选择此方法 `config` 构造函数的JSON对象。



<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 参数名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 值 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 参数值。 该值不能采用百分比编码。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
