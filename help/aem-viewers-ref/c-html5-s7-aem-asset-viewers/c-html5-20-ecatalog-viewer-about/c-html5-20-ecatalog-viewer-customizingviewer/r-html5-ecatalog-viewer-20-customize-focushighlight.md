---
title: 焦点高亮
description: 焦点查看器用户界面元素周围显示的输入焦点高亮。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5737d7-1295-46a9-9b84-c43269e5a914
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# 焦点高亮{#focus-highlight}

焦点查看器用户界面元素周围显示的输入焦点高亮。

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

焦点高亮显示的外观由以下CSS类选择器控制：

```
.s7ecatalogviewer *:focus
```

**焦点突出显示的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 大纲 </span> </p> </td> 
   <td colname="col2"> <p> 焦点高亮样式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要禁用所有查看器用户界面元素的默认浏览器焦点高亮显示，请将以下CSS选择器添加到查看器的样式表中：

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
