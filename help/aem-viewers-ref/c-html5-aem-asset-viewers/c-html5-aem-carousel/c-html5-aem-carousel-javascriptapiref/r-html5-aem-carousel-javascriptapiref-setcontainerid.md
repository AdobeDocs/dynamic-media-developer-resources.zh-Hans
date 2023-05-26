---
title: setContainerId
description: 轮播查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 32636cf9-3dc7-4299-a7b7-cf803ca36514
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 3%

---

# setContainerId{#setcontainerid}

轮播查看器的JavaScript API参考。

` setContainerId( *`containerId`*)`

设置DOM容器的ID(通常 `DIV`)，查看器将插入到其中。 无需在调用此方法时创建容器元素。 但是，在以下情况下必须存在容器： `init()` 运行。 必须在之前调用它 `init()`.

如果通过以下方式传递查看器配置信息，则可以选择此方法 `config` 构造函数的JSON对象。

## 参数 {#section-fa807db629ce43bab286b1e1dc96c492}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 容器的ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
