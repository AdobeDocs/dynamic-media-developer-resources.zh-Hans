---
description: 基本缩放、电子目录、电子目录搜索、弹出、内联缩放、混合媒体、旋转、视频、缩放、尺寸(3D)、传送、交互式图像、交互式视频和Video360查看器界面中公开的所有功能均可通过键盘访问。
solution: Experience Manager
title: 键盘辅助功能和导航
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
translation-type: tm+mt
source-git-commit: 62234233bb1a5bcbd0eac5d281b42ed785c0c169
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 键盘辅助功能和导航{#keyboard-accessibility-and-navigation}

基本缩放、电子目录、电子目录搜索、弹出、内联缩放、混合媒体、旋转、视频、缩放、旋转、尺寸(3D)、交互式图像、交互式视频和Video360查看器界面中公开的所有功能都可通过键盘访问。

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## 键盘辅助功能和导航{#topic-f5650e9493404e55a3627c8d1366b861}

基本缩放、电子目录、电子目录搜索、弹出、内联缩放、混合媒体、旋转、视频、缩放、旋转、尺寸(3D)、交互式图像、交互式视频和Video360查看器界面中公开的所有功能都可通过键盘访问。

最终用户可以使用&#x200B;**[!UICONTROL Tab]**&#x200B;和&#x200B;**[!UICONTROL Shift+Tab]**&#x200B;按键在查看器用户界面元素之间导航。 使用&#x200B;**[!UICONTROL Tab]**&#x200B;按Tab键顺序将输入焦点提前到下一个用户界面元素；使用&#x200B;**[!UICONTROL Shift+Tab]**&#x200B;将输入焦点返回到上一个用户界面元素。 焦点遍历遵循屏幕上自然的用户界面元素位置，并按从左到右、然后从上到下的顺序移动。

根据操作系统和Web浏览器设置，具有输入焦点的用户界面元素接收可视焦点指示。 例如，可视指示器可以是用户界面元素周围呈现的细边框。

可以在查看器CSS中禁用或自定义此类焦点突出显示。 在此帮助系统的目录中，在特定查看器名称（例如，基本缩放或交互式视频）下，单击&#x200B;**自定义查看器&#x200B;***的*名称>**&#x200B;焦点突出显示&#x200B;**。

在大多数情况下，单个查看器用户界面元素支持的按键效果显而易见，易于发现。

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>操作 </p> </th> 
   <th colname="col2" class="entry"> <p>按键 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>激活按钮组件 </p> </td> 
   <td colname="col2"> <p>空格键或Enter键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>放大或缩小 </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> 或 <span class="uicontrol"> - </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>缩放重置 </p> </td> 
   <td colname="col2"> <p>Esc键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>平移 </p> </td> 
   <td colname="col2"> <p>向上、向下、向左或向右箭头键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>旋转360度图像 </p> </td> 
   <td colname="col2"> <p>当图像处于重置状态时使用箭头键。 </p> <p>处理多维旋转集时使用向上或向下箭头键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>产品色板选择 </p> </td> 
   <td colname="col2"> <p>向上、向下、向左或向右箭头键；Home或End键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>产品色板激活 </p> </td> 
   <td colname="col2"> <p>空格键或Enter键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>视频和交互式视频，渐进倒回 </p> </td> 
   <td colname="col2"> <p>向左或向上箭头键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>视频和交互式视频，快速前进 </p> </td> 
   <td colname="col2"> <p>向右或向下箭头键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>视频和交互式视频，转到开头或结尾 </p> </td> 
   <td colname="col2"> <p>Home或End键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>视频和交互式视频，当焦点在滑块上时控制音量 </p> </td> 
   <td colname="col2"> <p>向上、向下、向左或向右箭头键；Home或End键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>视频和交互式视频，可变音量 </p> </td> 
   <td colname="col2"> <p>当焦点位于滑块部分上时，用于控制音量的箭头键、主键和结束键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>视频，当显示模态对话框时，焦点遍历仅限于对话框控件。 </p> </td> 
   <td colname="col2"> <p>Esc键关闭对话框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>传送，在主视图中更改横幅图像 </p> </td> 
   <td colname="col2"> <p>向左或向右箭头键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>传送、热点选择和热点激活 </p> </td> 
   <td colname="col2"> <p>热点选择：向上、向下、向左或向右箭头键 </p> <p>热点激活:空格键或Enter键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>电子目录，在主视图中更改页面图像 </p> </td> 
   <td colname="col2"> <p> 向左或向右箭头键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>电子目录，缩览图选择 </p> </td> 
   <td colname="col2"> <p>箭头键；Home和End键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>电子目录，色板激活 </p> </td> 
   <td colname="col2"> <p>空格键或Enter键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>电子目录，热点选择 </p> </td> 
   <td colname="col2"> <p>箭头键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>电子目录，激活 </p> </td> 
   <td colname="col2"> <p>空格键或Enter键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>电子目录，激活下拉组件 </p> </td> 
   <td colname="col2"> <p> 向下箭头键；空格键或Enter键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，当焦点位于拖放面板中时 </p> </td> 
   <td colname="col2"> <p>在激活面板之前，使用箭头键选择面板中的特定项目。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，当显示模态对话框时，焦点遍历仅限于对话框控件。 </p> </td> 
   <td colname="col2"> <p>Esc键关闭对话框。 </p> </td> 
  </tr> 
 </tbody> 
</table>
