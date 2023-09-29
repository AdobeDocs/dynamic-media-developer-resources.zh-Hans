---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>指定何时显示信息面板。 </p> <p>如果设置为 <span class="codeph"> 1</span>，则当鼠标进入图像映射区域(如果图像映射是非空的， <span class="codeph"> rollover_key</span> 属性)。 </p> <p>如果设置为 <span class="codeph"> 0</span>，则在选择图像映射（如果图像映射为非空）时，将触发信息面板 <span class="codeph"> rollover_key</span> 和空 <span class="codeph"> href</span> 属性)。 </p> <p> 在触控设备（包括支持触控的桌面系统）上忽略，并自动设置为 <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-ccfedc2da28f412a86d03f390db92b4b}

可选.

## 默认 {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## 示例 {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
