---
description: 焦点查看器用户界面元素周围显示的输入焦点突出显示。
seo-description: 焦点查看器用户界面元素周围显示的输入焦点突出显示。
seo-title: 焦点突出显示
solution: Experience Manager
title: 焦点突出显示
uuid: 50411b68-8d01-4240-b548-a6c51374a8c6
feature: Dynamic Media Classic，查看器，SDK/API，电子目录
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---


# 焦点高亮{#focus-highlight}

焦点查看器用户界面元素周围显示的输入焦点突出显示。

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

焦点高亮的外观由以下CSS类选择器控制：

```
.s7ecatalogviewer *:focus
```

**焦点突出显示的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 大纲  </span> </p> </td> 
   <td colname="col2"> <p> 焦点高亮样式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要禁用所有查看器用户界面元素的默认浏览器焦点突出显示，请将以下CSS选择器添加到查看器的样式表：

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

