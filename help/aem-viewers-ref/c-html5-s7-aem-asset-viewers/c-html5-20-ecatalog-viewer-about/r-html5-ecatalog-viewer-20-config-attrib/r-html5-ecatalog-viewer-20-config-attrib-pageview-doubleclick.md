---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog
role: Developer,User
exl-id: d53a8723-d710-4722-b1a7-c88d3b9d270b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# PageView.doubleclick{#pageview-doubleclick}

`[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|缩放|重置|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> 配置双击/点按以缩放操作的映射。 将设置为<span class="codeph">无</span>会禁用双击/点按缩放。 如果设置为<span class="codeph">缩放</span>，则单击图像会缩放一个缩放步骤；按住CTRL并单击可缩小一个缩放步骤。 将设置为<span class="codeph">重置</span>会导致单击图像，将缩放重置为初始缩放级别。 对于<span class="codeph"> zoomReset </span>，如果当前缩放因子达到或超过指定限制，则应用重置，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

可选。

## 默认 {#section-814d6bc6a0834005a0a72c7040e45693}

`reset` 台式计算机上； `zoomReset` 在触控设备上。

## 示例 {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
