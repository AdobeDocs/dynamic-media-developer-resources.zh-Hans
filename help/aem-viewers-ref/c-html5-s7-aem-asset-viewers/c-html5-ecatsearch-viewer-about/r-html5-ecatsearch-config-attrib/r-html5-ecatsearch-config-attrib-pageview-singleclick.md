---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffe77be7-bf12-4e9d-9355-2857d366d14e
TQID: 'https://experienceleague.adobe.com/5EsGuAIb9PP4apehGQmEvHT4blmS5I9K--bSALwwpM8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 94
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

