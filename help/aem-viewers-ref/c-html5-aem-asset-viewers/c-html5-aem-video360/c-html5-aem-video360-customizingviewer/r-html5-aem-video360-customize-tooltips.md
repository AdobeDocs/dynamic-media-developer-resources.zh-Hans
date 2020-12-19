---
description: 在桌面系统上，一些用户界面元素（如按钮）具有鼠标悬停时显示的工具提示。
seo-description: 在桌面系统上，一些用户界面元素（如按钮）具有鼠标悬停时显示的工具提示。
seo-title: 工具提示
solution: Experience Manager
title: 工具提示
topic: Dynamic media
uuid: 37ce59fe-f1f5-4226-af2e-5183ea8b7647
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 5%

---


# 工具提示{#tooltips}

在桌面系统上，一些用户界面元素（如按钮）具有鼠标悬停时显示的工具提示。

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
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p> 背景颜色. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>文本颜色. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列  </span> </p> </td> 
   <td colname="col2"> <p>文本字体名称. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字号  </span> </p> </td> 
   <td colname="col2"> <p>文本字体大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>如果工具提示样式是从嵌入网页中自定义的，则所有属性都必须包含`!IMPORTANT`规则。 如果在查看器的CSS文件中自定义了工具提示，则不必这样做。

示例——要设置工具提示，其中灰色边框具有三个像素圆角半径、黑色背景和以Arial、11像素表示的白色文本：

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

