---
title: 键盘辅助功能和导航
description: 基本缩放、eCatalog、eCatalog搜索、弹出、内联缩放、混合媒体、旋转、视频、缩放、维度(3D)、轮播、交互式图像、交互式视频和Video360查看器界面中公开的所有功能均可使用键盘。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# 键盘辅助功能和导航{#keyboard-accessibility-and-navigation}

基本缩放、eCatalog、eCatalog搜索、弹出、内联缩放、混合媒体、旋转、视频、缩放、轮播、维度(3D)、交互式图像、交互式视频和Video360查看器界面中公开的所有功能均可使用键盘。

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## 键盘辅助功能和导航 {#topic-f5650e9493404e55a3627c8d1366b861}

基本缩放、eCatalog、eCatalog搜索、弹出、内联缩放、混合媒体、旋转、视频、缩放、轮播、维度(3D)、交互式图像、交互式视频和Video360查看器界面中公开的所有功能均可使用键盘。

最终用户可以使用 **[!UICONTROL 选项卡]** 和 **[!UICONTROL Shift+Tab]** 击键。 使用 **[!UICONTROL 选项卡]** 按Tab键顺序将输入焦点提前到下一个用户界面元素；使用 **[!UICONTROL Shift+Tab]** 将输入焦点重新引回到上一个用户界面元素。 焦点遍历遵循屏幕上自然的用户界面元素位置，并按从左到右、从上到下的顺序移动。

根据操作系统和Web浏览器设置，具有输入焦点的用户界面元素接收可视焦点指示。 例如，可视指示器可以是围绕用户界面元素呈现的细边框。

可以在查看器CSS中禁用或自定义此类焦点突出显示。 在此帮助系统的目录中，在特定查看器名称（例如，“基本缩放”或“交互式视频”）下，单击 **自定义 *查看器名称*** >**&#x200B;焦点突出显示&#x200B;**.

单个查看器用户界面元素支持的击键在大多数情况下是显而易见的，并且易于发现。

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>操作 </p> </th> 
   <th colname="col2" class="entry"> <p>击键 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>激活按钮组件 </p> </td> 
   <td colname="col2"> <p>空格键或Enter键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>放大或缩小 </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> 或 <span class="uicontrol"> - </span>，分别为。 </p> </td> 
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
   <td colname="col2"> <p>当图像处于重置状态时，使用箭头键。 </p> <p>使用多维旋转集时，请使用向上或向下箭头键。 </p> </td> 
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
   <td colname="col1"> <p>视频和交互式视频，逐步倒带 </p> </td> 
   <td colname="col2"> <p>向左或向上箭头键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>视频和交互式视频，快速前进 </p> </td> 
   <td colname="col2"> <p>向右或向下箭头键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>视频和交互式视频，转到开始或结束 </p> </td> 
   <td colname="col2"> <p>Home或End键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>视频和交互式视频，在焦点位于滑块上时控制音量 </p> </td> 
   <td colname="col2"> <p>向上、向下、向左或向右箭头键；Home或End键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>视频和交互式视频，音量可变 </p> </td> 
   <td colname="col2"> <p>当焦点位于其滑块部分上时，用于控制音量的箭头、主键和结束键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>视频中，当显示模式对话框时，焦点遍历将限制为仅显示对话框控件。 </p> </td> 
   <td colname="col2"> <p>Esc键关闭对话框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>轮播，在主视图中更改横幅图像 </p> </td> 
   <td colname="col2"> <p>向左或向右箭头键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>轮播、热点选择和热点激活 </p> </td> 
   <td colname="col2"> <p>热点选择：向上、向下、向左或向右箭头键 </p> <p>热点激活：空格键或Enter键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog中，在主视图中更改页面图像 </p> </td> 
   <td colname="col2"> <p> 向左或向右箭头键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>电子目录、缩略图选择 </p> </td> 
   <td colname="col2"> <p>箭头键；Home和End键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，样本激活 </p> </td> 
   <td colname="col2"> <p>空格键或Enter键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>电子目录、热点选择 </p> </td> 
   <td colname="col2"> <p>箭头键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，激活 </p> </td> 
   <td colname="col2"> <p>空格键或Enter键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，激活下拉组件 </p> </td> 
   <td colname="col2"> <p> 向下箭头键；空格键或Enter键。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，焦点位于拖放式面板中时 </p> </td> 
   <td colname="col2"> <p>在激活面板之前，使用箭头键选择面板中的特定项目。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，当显示模态对话框时，焦点遍历将限制为仅显示对话框控件。 </p> </td> 
   <td colname="col2"> <p>Esc键关闭对话框。 </p> </td> 
  </tr> 
 </tbody> 
</table>
