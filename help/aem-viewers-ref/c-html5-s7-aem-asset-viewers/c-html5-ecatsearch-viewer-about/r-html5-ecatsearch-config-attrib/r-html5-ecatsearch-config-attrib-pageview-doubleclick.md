---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# PageView.doubleclick{#pageview-doubleclick}

[!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> 配置多次单击/点按以缩放操作的映射。 设置为<span class="codeph">无</span>将禁用多次单击/点按缩放。 如果设置为<span class="codeph">缩放</span>，则单击图像将放大一个缩放步骤；按住CTRL并单击可缩小一个缩放步骤。 设置为<span class="codeph"> reset </span>会导致单击图像将缩放重置为初始缩放级别。 对于<span class="codeph"> zoomReset </span>，如果当前缩放因子达到或超过指定限制，则应用reset，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

可选。

## 默认 {#section-814d6bc6a0834005a0a72c7040e45693}

[!DNL `reset`] 在台式计算机上； [!DNL `zoomReset`] 触控设备。

## 示例 {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
