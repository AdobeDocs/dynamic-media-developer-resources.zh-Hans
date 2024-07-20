---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffe77be7-bf12-4e9d-9355-2857d366d14e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 配置单击/点按到缩放操作的映射。 设置为<span class="codeph">无</span>可禁用单击/点按缩放。 如果设置为<span class="codeph">缩放</span>，则单击图像可将其放大一个缩放步长；按住CTRL键单击可将其缩小一个缩放步长。 设置为<span class="codeph">重置</span>会导致单击图像以将缩放重置为初始缩放级别。 对于<span class="codeph"> zoomReset </span>，如果当前缩放因子达到或超过指定限制，则应用重置，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-edcfcd6c0bd24ac093442c56450b3c97}

可选.

## 默认 {#section-58cbfe8a90214c49bbbfb7e83c569d75}

桌面计算机上的[!DNL `zoomReset`]；触控设备上的[!DNL `none`]。

## 示例 {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]
