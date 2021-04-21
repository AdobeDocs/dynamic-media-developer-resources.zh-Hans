---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---


# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> 配置单击/点按缩放操作的映射。设置为<span class="codeph">无</span>将禁用单击/点按缩放。 如果设置为<span class="codeph">缩放</span>，则单击图像将放大一个缩放步骤；按住CTRL并单击可缩小一个缩放步骤。 设置为<span class="codeph"> reset </span>会导致单击图像将缩放重置为初始缩放级别。 对于<span class="codeph"> zoomReset </span>，如果当前缩放因子达到或超过指定限制，则应用reset，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-edcfcd6c0bd24ac093442c56450b3c97}

可选。

## 默认 {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` 在台式计算机上； `none` 触控设备。

## 示例 {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
