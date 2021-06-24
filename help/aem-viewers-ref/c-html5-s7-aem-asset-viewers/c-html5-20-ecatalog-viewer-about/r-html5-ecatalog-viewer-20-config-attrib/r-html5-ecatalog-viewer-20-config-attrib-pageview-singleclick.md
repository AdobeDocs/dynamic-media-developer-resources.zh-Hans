---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog
role: Developer,Business Practitioner
exl-id: 96896145-f8d9-4fee-abfe-7f9193776993
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|缩放|重置|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> 配置单击/点按以缩放操作的映射。将设置为<span class="codeph">无</span>会禁用单击/点按缩放。 如果设置为<span class="codeph">缩放</span>，则单击图像会缩放一个缩放步骤；按住CTRL并单击可缩小一个缩放步骤。 将设置为<span class="codeph">重置</span>会导致单击图像，将缩放重置为初始缩放级别。 对于<span class="codeph"> zoomReset </span>，如果当前缩放因子达到或超过指定限制，则应用重置，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-edcfcd6c0bd24ac093442c56450b3c97}

可选。

## 默认 {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` 台式计算机上； `none` 在触控设备上。

## 示例 {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
