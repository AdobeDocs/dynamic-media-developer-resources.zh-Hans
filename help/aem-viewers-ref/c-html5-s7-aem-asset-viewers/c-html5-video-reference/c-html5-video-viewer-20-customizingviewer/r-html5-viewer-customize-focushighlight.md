---
description: 通过CSS类选择器控制在聚焦的查看器UI元素周围显示的输入焦点突出显示。
seo-description: 通过CSS类选择器控制在聚焦的查看器UI元素周围显示的输入焦点突出显示。
seo-title: 焦点突出显示
solution: Experience Manager
title: 焦点突出显示
topic: Dynamic media
uuid: cf5acb11-168e-4303-a637-d959687a0548
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 焦点突出显示{#focus-highlight}

通过CSS类选择器控制在聚焦的查看器UI元素周围显示的输入焦点突出显示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS属性**

使用以下CSS类选择器控制外观：

```
.s7videoviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> 轮廓 </span> </p> </td> 
   <td colname="col2"> <p>焦点突出显示样式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——要禁用所有查看器用户界面元素的默认浏览器焦点突出显示，请将以下CSS选择器添加到查看器的样式表：

```
.s7videoviewer *:focus { 
 outline: none; 
}
```

