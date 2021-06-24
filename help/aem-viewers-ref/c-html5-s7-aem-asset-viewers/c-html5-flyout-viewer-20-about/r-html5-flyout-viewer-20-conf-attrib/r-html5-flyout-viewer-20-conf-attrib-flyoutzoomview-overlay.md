---
description: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
feature: Dynamic Media Classic，查看器，SDK/API，弹出
role: Developer,Business Practitioner
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 控制弹出窗口处于活动状态时的主视图高亮显示外观。 当设置为<span class="codeph"> 0</span>时，弹出窗口中当前可见的区域将使用<span class="codeph"> .s7highlight</span>或<span class="codeph"> .s7cursor</span> CSS类名称（取决于<span class="codeph"> highlightmode</span>修饰符的值）提供的样式高亮显示。 当设置为<span class="codeph"> 1</span>组件进入“反向”模式时，当前查看的区域要么完全透明（如果设置为<span class="codeph"> highlightmode</span>，则设置为<span class="codeph"> highlight</span>），要么设置为<span class="codeph"> .s7cursor</span> CSS类名称（如果设置为<span class="codeph"> highlightmode</span>，则设置为<span class="codeph"></span>），但周围区域使用<span class="codeph">叠加提供的样式填充CSS类名称。</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选。

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
