---
description: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
uuid: e6e9e97c-5d9b-47ca-bae3-ed3371c5ff9b
feature: Dynamic Media Classic，查看器，SDK/API，弹出
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 4%

---


# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 控制弹出处于活动状态时的主视图高亮外观。 当设置为<span class="codeph"> 0</span>时，将使用<span class="codeph"> .s7highlight</span>或<span class="codeph"> .s7cursor</span> CSS类名称（取决于<span class="codeph"> highlightmode</span>修饰符的值）提供的样式高亮显示弹出窗口中当前可见的区域。 当设置为<span class="codeph"> 1</span>组件时，进入“反向”模式，其中当前查看的区域为完全透明（如果<span class="codeph"> highlightmode</span>设置为<span class="codeph"> highlight</span>）或使用<span class="codeph"> .s7cursor</span> CSS类名称设置样式（如果<span class="codeph"> highlightmode</span>设置为<span class="codeph"> cursor</span>），但使用<span class="codeph"> .s7overlay</span> CSS类名提供的样式填充周围区域。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选。

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
