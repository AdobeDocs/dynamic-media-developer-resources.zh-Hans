---
description: 通过CSS类选择器控制焦点查看器UI元素周围显示的输入焦点高亮。
seo-description: 通过CSS类选择器控制焦点查看器UI元素周围显示的输入焦点高亮。
seo-title: 焦点突出显示
solution: Experience Manager
title: 焦点突出显示
uuid: 56600f9c-c51e-40a4-93b6-a43902ef5ff1
feature: Dynamic Media Classic，查看器，SDK/API，交互式图像
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# 焦点高亮{#focus-highlight}

通过CSS类选择器控制焦点查看器UI元素周围显示的输入焦点高亮。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS属性**

使用以下CSS类选择器控制外观：

```
.s7interactiveimage *:focus
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
   <td colname="col2"> <p>焦点高亮样式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要禁用所有查看器用户界面元素的默认浏览器焦点突出显示，请将以下CSS选择器添加到查看器的样式表：

```
.s7interactiveimage *:focus { 
 outline: none; 
}
```

