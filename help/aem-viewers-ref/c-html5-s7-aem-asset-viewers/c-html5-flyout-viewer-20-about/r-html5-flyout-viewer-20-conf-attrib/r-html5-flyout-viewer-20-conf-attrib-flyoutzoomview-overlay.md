---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 控制弹出窗口处于活动状态时的主视图高亮显示外观。 当设置为 <span class="codeph"> 0</span>，则弹出窗口中当前可见的区域将使用提供的样式突出显示 <span class="codeph"> .s7高亮显示</span> 或 <span class="codeph"> .s7cursor</span> CSS类名称(取决于 <span class="codeph"> 高光模式</span> 修饰符)。 当设置为 <span class="codeph"> 1</span> 组件进入“反向”模式，其中当前查看的区域要么完全透明（如果是） <span class="codeph"> 高光模式</span> 设置为 <span class="codeph"> 突出显示</span>)或样式为 <span class="codeph"> .s7cursor</span> CSS类名称（大小写） <span class="codeph"> 高光模式</span> 设置为 <span class="codeph"> 光标</span>)，但周围区域会使用 <span class="codeph"> .s7叠加</span> CSS类名称。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选。

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
