---
title: 焦点高亮
description: 焦点查看器UI元素周围显示的输入焦点高亮通过CSS类选择器进行控制。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 242b80db-f5b4-44ad-9169-bd6ecf859ed0
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# 焦点高亮{#focus-highlight}

焦点查看器UI元素周围显示的输入焦点高亮通过CSS类选择器进行控制。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS属性**

外观由以下CSS类选择器控制：

```
.s7smartcropvideoviewer *:focus
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">大纲</span> </p> </td> 
   <td colname="col2"> <p>焦点突出显示样式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要禁用所有查看器用户界面元素的默认浏览器焦点高亮显示，请将以下CSS选择器添加到查看器的样式表中：

```
.s7smartcropvideoviewer *:focus { 
 outline: none; 
}
```
