---
description: 页面指示器显示当前页面索引和总页面计数。 它显示在桌面系统和平板电脑的主控制栏中，在手机上，它被添加到辅助控制栏中。 页面指示符可以由CSS调整大小、设计外观和定位。
seo-description: 页面指示器显示当前页面索引和总页面计数。 它显示在桌面系统和平板电脑的主控制栏中，在手机上，它被添加到辅助控制栏中。 页面指示符可以由CSS调整大小、设计外观和定位。
seo-title: 页面指示器
solution: Experience Manager
title: 页面指示器
topic: Dynamic media
uuid: 1be6021b-3026-48ef-b121-eeb8270d2bae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 页面指示器{#page-indicator}

页面指示器显示当前页面索引和总页面计数。 它显示在桌面系统和平板电脑的主控制栏中，在手机上，它被添加到辅助控制栏中。 页面指示符可以由CSS调整大小、设计外观和定位。

使用以下CSS类选择器控制外观页面指示符：

`.s7ecatalogsearchviewer .s7pageindicator`

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
   <td colname="col2"> <p>从主控制栏（在桌面系统和平板电脑上）或辅助控制栏（在手机上）的上边框的位置，包括边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>从主控制栏（在桌面系统和平板电脑上）或辅助控制栏（在手机上）的右边框定位，包括边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p>从主控制栏（在桌面系统和平板电脑上）或辅助控制栏（在手机上）的左边框中的位置，包括边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>从主控制栏（在桌面系统和平板电脑上）或辅助控制栏（在手机上）的下边框中的位置，包括边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>页面指示器的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>页面指示符的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>字体颜色. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列 </span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小 </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置一个56 x 28像素的页面指示符，它位于水平居中，距主控件栏底部有4个像素，并使用14像素的Helvetica字体。

```
.s7ecatalogsearchviewer  .s7pageindicator { 
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

