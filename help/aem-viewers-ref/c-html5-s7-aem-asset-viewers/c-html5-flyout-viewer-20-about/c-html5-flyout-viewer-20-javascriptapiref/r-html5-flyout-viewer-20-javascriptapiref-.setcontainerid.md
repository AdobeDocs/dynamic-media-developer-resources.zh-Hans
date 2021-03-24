---
description: 弹出查看器的JavaScript API参考。
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic，查看器，SDK/API，弹出
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---


# setContainerId{#setcontainerid}

弹出查看器的JavaScript API参考。

` setContainerId( *`containerId`*)`

设置DOM容器的ID（通常为`DIV`），查看器将插入其中。 调用此方法时不必创建容器元素。 但是，运行`init()`时必须存在容器。 必须在`init()`之前调用它。 如果将查看器配置信息与`config` JSON对象一起传递到构造函数，则此方法是可选的。

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

