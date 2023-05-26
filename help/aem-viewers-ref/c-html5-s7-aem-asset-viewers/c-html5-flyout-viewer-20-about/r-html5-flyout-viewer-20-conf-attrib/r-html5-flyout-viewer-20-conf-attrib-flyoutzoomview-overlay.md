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
ht-degree: 3%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 控制弹出窗口处于活动状态时的主视图高亮显示。 当设置为 <span class="codeph"> 0</span>，则当前在弹出窗口中可见的区域会使用提供的样式突出显示 <span class="codeph"> .s7高亮</span> 或 <span class="codeph"> .s7cursor</span> CSS类名称(取决于 <span class="codeph"> highlightmode</span> modifier)。 当设置为 <span class="codeph"> 1</span> 组件进入“反向”模式，当前查看的区域完全透明(如果是 <span class="codeph"> highlightmode</span> 设置为 <span class="codeph"> 高亮</span>)或样式为 <span class="codeph"> .s7cursor</span> CSS类名称(大写 <span class="codeph"> highlightmode</span> 设置为 <span class="codeph"> 光标</span>)，但周围区域使用提供的样式填充 <span class="codeph"> .s7overlay</span> CSS类名称。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选.

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
