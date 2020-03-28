---
description: 用于视频图像查看器的JavaScript API参考。
seo-description: 用于视频图像查看器的JavaScript API参考。
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: f1486f82-28dd-4321-a0e5-9e5696f6bbf7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setContainerId{#setcontainerid}

用于视频图像查看器的JavaScript API参考。

` setContainerId( *`containerId`*)`

设置将查看器插入其中的DOM容器（通常是DIV）的ID。 无需在调用此方法之前创建容器元素。 但是，运行时必须存 `init()` 在容器。 必须在之前调用 `init()`。

如果查看器配置信息与 `config` JSON对象一起传递到构造函数，则此方法是可选的。

## 参数 {#section-fa807db629ce43bab286b1e1dc96c492}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 容 <span class="varname"> 器ID </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 容器ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

