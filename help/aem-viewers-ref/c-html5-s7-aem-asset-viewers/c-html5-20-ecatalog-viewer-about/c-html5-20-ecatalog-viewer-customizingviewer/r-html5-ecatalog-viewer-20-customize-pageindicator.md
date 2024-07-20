---
title: 页面指示器
description: 页面指示器显示当前页面索引和页面总数。 它显示在桌面系统和平板电脑的主控制栏中，在手机上则被添加到辅助控制栏中。 页面指示器可以由CSS调整大小、设置外观和进行定位。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: c63af583-274c-4052-8186-604119a368af
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# 页面指示器{#page-indicator}

页面指示器显示当前页面索引和页面总数。 它显示在桌面系统和平板电脑的主控制栏中，在手机上则被添加到辅助控制栏中。 页面指示器可以由CSS调整大小、设置外观和进行定位。

页面指示器的外观由以下CSS类选择器控制：

`.s7ecatalogviewer .s7pageindicator`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p>位于主控制栏（在桌面系统和平板电脑上）或辅助控制栏（在手机上）的顶部边框，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p>从主控制栏（在桌面系统和平板电脑上）或辅助控制栏（在手机上）的右边框定位，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">已离开</span> </p> </td> 
   <td colname="col2"> <p>从主控制栏（在桌面系统和平板电脑上）或辅助控制栏（在手机上）的左边框定位，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">后</span> </p> </td> 
   <td colname="col2"> <p>从主控制栏（在桌面系统和平板电脑上）或辅助控制栏（在手机上）的底部边框定位，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>页面指示器的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>页面指示器的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p>字体颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>字体大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置一个页面指示器，其大小为56 x 28像素，水平居中并从主控制栏底部放置4像素，并使用14像素的Helvetica®字体。

```
.s7ecatalogviewer  .s7pageindicator { 
 position:absolute; 
 bottom: 4px; 
 margin-left: -28px;  
 left: 50%; 
 width:56px; 
 height:28px; 
 font-family: Helvetica; 
 font-size:14px; 
}
```
