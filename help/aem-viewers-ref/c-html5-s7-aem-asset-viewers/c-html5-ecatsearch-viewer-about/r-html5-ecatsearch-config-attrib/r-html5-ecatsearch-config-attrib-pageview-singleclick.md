---
description: 'null'
seo-description: 'null'
seo-title: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
topic: Dynamic media
uuid: b08b605e-5ffc-42cc-931d-d67750a8dca8
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 6%

---


# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|缩放|重置|缩放重置  </span> </p> </td> 
   <td colname="col2"> <p> 配置单击／点按缩放操作的映射。设置为<span class="codeph">无</span>将禁用单击／点按缩放。 如果设置为<span class="codeph">缩放</span>单击图像，则会放大一个缩放步骤；按住CTRL并单击可缩小一个缩放步骤。 将设置为<span class="codeph"> reset </span>会导致单击图像将缩放重置为初始缩放级别。 对于<span class="codeph"> zoomReset </span>，如果当前缩放因子达到或超过指定限制，则应用reset，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-edcfcd6c0bd24ac093442c56450b3c97}

可选。

## 默认 {#section-58cbfe8a90214c49bbbfb7e83c569d75}

[!DNL `zoomReset`] 在台式计算机上； [!DNL `none`] 触控设备。

## 示例 {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]