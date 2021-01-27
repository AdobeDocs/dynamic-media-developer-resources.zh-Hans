---
description: 页面指示器显示当前页面索引和总页面计数。 它显示在台式机系统和平板电脑的主控制栏中，在手机上则添加到辅助控制栏中。 页面指示器可由CSS调整大小、设计外观和定位。
seo-description: 页面指示器显示当前页面索引和总页面计数。 它显示在台式机系统和平板电脑的主控制栏中，在手机上则添加到辅助控制栏中。 页面指示器可由CSS调整大小、设计外观和定位。
seo-title: 页面指示器
solution: Experience Manager
title: 页面指示器
topic: Dynamic Media
uuid: 5e33c149-fdc7-419a-b5ff-b9be3f342d9f
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 4%

---


# 页面指示器{#page-indicator}

页面指示器显示当前页面索引和总页面计数。 它显示在台式机系统和平板电脑的主控制栏中，在手机上则添加到辅助控制栏中。 页面指示器可由CSS调整大小、设计外观和定位。

页面指示符的外观由以下CSS类选择器控制：

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
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>从主控制栏（在台式机系统和平板电脑上）或辅助控制栏（在手机上）的上边框进行定位，包括边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>从主控制栏（在台式机系统和平板电脑上）或辅助控制栏（在手机上）的右边框中定位，包括边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p>从主控制栏（在台式机系统和平板电脑上）或辅助控制栏（在手机上）的左边框中的位置，包括边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>从主控制栏（在台式机系统和平板电脑上）或辅助控制栏（在手机上）的下边框进行定位，包括边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>页面指示器的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>页面指示器的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>字体颜色. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列  </span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字号  </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置一个56 x 28像素的页面指示符，其水平居中并位于距主控件条底部4像素的位置，并使用14像素的Helvetica字体。

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

