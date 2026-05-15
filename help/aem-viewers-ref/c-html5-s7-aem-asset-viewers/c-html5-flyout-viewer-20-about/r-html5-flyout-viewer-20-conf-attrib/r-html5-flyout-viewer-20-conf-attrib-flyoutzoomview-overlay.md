---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
TQID: 'https://experienceleague.adobe.com/MxdOr4hM38H7Hy6uCIvrOJQ0xjxbiyaJlIwaIFKGZOU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 4%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> 控制弹出项处于活动状态时主视图的加亮外观。 当设置为<span class="codeph"> 0</span>时，弹出窗口中当前可见的区域将使用<span class="codeph"> .s7highlight</span>或<span class="codeph"> .s7cursor</span> CSS类名提供的样式高亮显示（具体取决于<span class="codeph"> highlightmode</span>修饰符的值）。 当设置为<span class="codeph">时，1</span>组件进入“反向”模式，当前查看的区域要么完全透明（如果<span class="codeph"> highlightmode</span>设置为<span class="codeph"> highlightmode</span>），要么使用<span class="codeph"> .s7cursor</span> CSS类名称设置样式（如果<span class="codeph"> highlightmode</span>设置为<span class="codeph"> cursor</span>），但周围的区域已使用<span class="codeph"> .s7overlay</span> CSS类名称提供的样式填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选.

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
