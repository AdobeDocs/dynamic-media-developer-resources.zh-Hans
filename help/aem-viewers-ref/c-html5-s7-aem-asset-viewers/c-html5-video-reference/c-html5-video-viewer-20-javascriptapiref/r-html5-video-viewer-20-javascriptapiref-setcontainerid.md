---
description: 视频查看器的JavaScript API参考。
seo-description: 视频查看器的JavaScript API参考。
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: a4b741a1-b0b3-4bc3-aeab-9d0e44ec4e79
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 2%

---


# setContainerId{#setcontainerid}

视频查看器的JavaScript API参考。

` setContainerId( *`containerId`*)`

设置查看器插入的DOM容器的ID（通常为`DIV`）。 调用此方法时，不必创建容器元素。 但是，运行`init()`时必须存在容器。 此参数在`init()`之前调用。 如果将查看器配置信息与`config` JSON对象一起传递给构造函数，则此方法是可选的。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 容器ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

