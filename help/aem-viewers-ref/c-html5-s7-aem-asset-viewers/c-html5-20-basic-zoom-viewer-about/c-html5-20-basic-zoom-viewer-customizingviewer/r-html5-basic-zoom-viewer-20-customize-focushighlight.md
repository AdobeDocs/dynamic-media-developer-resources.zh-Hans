---
description: 通过CSS类选择器控制聚焦查看器使用界面元素周围显示的输入焦点突出显示。
seo-description: 通过CSS类选择器控制聚焦查看器使用界面元素周围显示的输入焦点突出显示。
seo-title: 焦点突出显示
solution: Experience Manager
title: 焦点突出显示
topic: Dynamic Media
uuid: 1b552aec-837a-4df4-91dc-615ceead92b3
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 1%

---


# 焦点突出显示{#focus-highlight}

通过CSS类选择器控制聚焦查看器使用界面元素周围显示的输入焦点突出显示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

外观由以下CSS类选择器控制：

```
.s7basiczoomviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> 大纲  </span> </p> </td> 
   <td colname="col2"> <p>焦点突出显示样式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——要禁用所有查看器用户界面元素的默认浏览器焦点突出显示，请将以下CSS选择器添加到查看器的样式表：

```
.s7basiczoomviewer *:focus { 
 outline: none; 
}
```

