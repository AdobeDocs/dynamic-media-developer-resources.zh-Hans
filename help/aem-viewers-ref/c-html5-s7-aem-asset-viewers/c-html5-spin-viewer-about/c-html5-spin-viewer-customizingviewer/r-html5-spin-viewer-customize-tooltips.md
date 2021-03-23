---
description: 在桌面系统上，某些用户界面元素（如按钮）具有鼠标悬停时显示的工具提示。
seo-description: 在桌面系统上，某些用户界面元素（如按钮）具有鼠标悬停时显示的工具提示。
seo-title: 工具提示
solution: Experience Manager
title: 工具提示
uuid: f5c2c648-ce1d-401f-9c26-7b5b79438738
feature: Dynamic Media Classic，查看器，SDK/API，旋转集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 5%

---


# 工具提示{#tooltips}

在桌面系统上，某些用户界面元素（如按钮）具有鼠标悬停时显示的工具提示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

工具提示的外观由以下CSS类选择器控制：

```
.s7tooltip
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
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> 背景边框半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边框颜色  </span> </p> </td> 
   <td colname="col2"> <p> 背景边框颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 背景颜色. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>文本颜色. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>文本字体名称. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小  </span> </p> </td> 
   <td colname="col2"> <p>文本字体大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>如果工具提示样式是从嵌入网页中自定义的，则所有属性必须包含`!IMPORTANT`规则。 如果在查看器的CSS文件中自定义了工具提示，则不必这样做。

示例 — 设置工具提示，其中的灰色边框具有3px圆角半径、黑色背景和用Arial文件编写的白色文本，大小为11像素：

```
.s7tooltip { 
 border-radius: 3px 3px 3px 3px; 
 border-color: #999999; 
 background-color: #000000; 
 color: #FFFFFF; 
 font-family: Arial, Helvetica, sans-serif; 
 font-size: 11px; 
}
```

