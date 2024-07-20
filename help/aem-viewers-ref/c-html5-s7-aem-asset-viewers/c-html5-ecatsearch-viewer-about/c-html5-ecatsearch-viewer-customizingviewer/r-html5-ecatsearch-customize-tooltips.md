---
title: 工具提示
description: 在桌面系统上，某些用户界面元素（如按钮）具有在鼠标悬停时显示的工具提示。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0350bdbc-3e3d-4bc0-98f6-5d7bf4121d9a
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# 工具提示{#tooltips}

在桌面系统上，某些用户界面元素（如按钮）具有在鼠标悬停时显示的工具提示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

主查看器区域的&#x200B;**CSS属性**

使用以下CSS类选择器控制工具提示的外观：

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
   <td colname="col1"> <p> <span class="codeph">边框半径</span> </p> </td> 
   <td colname="col2"> <p> 背景边框半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边框颜色</span> </p> </td> 
   <td colname="col2"> <p> 背景边框颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p>文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>文本字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>文本字体大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>如果工具提示样式是从嵌入网页中自定义的，则所有属性都必须包含`!IMPORTANT`规则。 如果在查看器的CSS文件中自定义了工具提示，则无需使用此规则。

示例 — 要设置具有3像素圆角半径的灰色边框、黑色背景和使用Arial®编写的白文本（11像素大小）的工具提示：

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
