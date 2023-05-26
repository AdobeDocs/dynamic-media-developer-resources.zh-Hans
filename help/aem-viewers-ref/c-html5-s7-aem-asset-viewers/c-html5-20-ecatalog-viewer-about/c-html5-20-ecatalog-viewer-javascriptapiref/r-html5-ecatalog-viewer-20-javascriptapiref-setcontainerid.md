---
title: setContainerId
description: eCatalog查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 32e75d36-cc9a-42df-95e8-5b48456296e9
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

eCatalog查看器的JavaScript API参考。

` setContainerId( *`containerId`*)`

设置的ID `DOM` 容器(通常为 `DIV`)，查看器将插入到其中。 无需在调用此方法时创建容器元素。 但是，在以下情况下必须存在容器： `init()` 运行。 必须在之前调用它 `init()`.

如果通过以下方式传递查看器配置信息，则可以选择此方法 `config` 构造函数的JSON对象。

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
