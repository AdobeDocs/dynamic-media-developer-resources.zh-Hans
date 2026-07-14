---
description: eCatalog查看器的JavaScript API参考。
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: f1491091-f109-4836-b7f1-ad0619b72dce
TQID: 'https://experienceleague.adobe.com/IYNuZDz6uNspQbYv4nqBn5bUFD6y5BwRwUkrNvLVoMM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 84
ht-degree: 2%

---

# setContainerId{#setcontainerid}

eCatalog查看器的JavaScript API参考。

[!DNL ` setContainerId( *`containerId`*)`]

设置查看器插入到其中的`DOM`容器（通常为`DIV`）的ID。 在调用此方法时，无需创建容器元素。 但是，运行`init()`时容器必须存在。 必须在`init()`之前调用它。

如果将查看器配置信息与`config` JSON对象一起传递给构造函数，则此方法是可选的。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}容器的</span> ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例： {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
