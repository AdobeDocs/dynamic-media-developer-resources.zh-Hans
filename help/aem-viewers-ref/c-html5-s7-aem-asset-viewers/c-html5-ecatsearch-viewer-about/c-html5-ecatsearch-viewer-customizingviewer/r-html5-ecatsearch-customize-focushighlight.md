---
description: 在焦点查看器用户界面元素周围显示输入焦点突出显示。
solution: Experience Manager
title: 焦点突出显示
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog搜索
role: Developer,Business Practitioner
exl-id: 949b8a8b-5f59-415e-acc1-bf8cea77cbd9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# 焦点突出显示{#focus-highlight}

在焦点查看器用户界面元素周围显示输入焦点突出显示。

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

焦点突出显示的外观通过以下CSS类选择器进行控制：

```
.s7ecatalogviewer *:focus
```

**焦点突出显示的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 大纲  </span> </p> </td> 
   <td colname="col2"> <p> 焦点突出显示样式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要禁用所有查看器用户界面元素的默认浏览器焦点突出显示，请将以下CSS选择器添加到查看器的样式表中：

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
