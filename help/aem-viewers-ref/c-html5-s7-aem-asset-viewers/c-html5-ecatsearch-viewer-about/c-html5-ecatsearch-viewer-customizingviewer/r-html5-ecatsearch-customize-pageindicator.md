---
description: 页面指示器显示当前页面索引和总页数。 它显示在台式机系统和平板电脑的主控制栏中，在手机上，它添加到辅助控制栏。 页面指示器可以通过CSS进行大小调整、外观设置和定位。
seo-description: 页面指示器显示当前页面索引和总页数。 它显示在台式机系统和平板电脑的主控制栏中，在手机上，它添加到辅助控制栏。 页面指示器可以通过CSS进行大小调整、外观设置和定位。
seo-title: 页面指示器
solution: Experience Manager
title: 页面指示器
uuid: 1be6021b-3026-48ef-b121-eeb8270d2bae
feature: Dynamic Media Classic，查看器，SDK/API，电子目录搜索
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 3%

---


# 页面指示器{#page-indicator}

页面指示器显示当前页面索引和总页数。 它显示在台式机系统和平板电脑的主控制栏中，在手机上，它添加到辅助控制栏。 页面指示器可以通过CSS进行大小调整、外观设置和定位。

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
   <td colname="col2"> <p>从主控制栏（在台式机系统和平板电脑上）或辅助控制栏（在手机上）的底边框中的位置，包括边距。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小  </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置一个56 x 28像素的页面指示器，水平居中并位于距主控件条底部4像素的位置，然后使用14像素的Helvetica字体。

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

