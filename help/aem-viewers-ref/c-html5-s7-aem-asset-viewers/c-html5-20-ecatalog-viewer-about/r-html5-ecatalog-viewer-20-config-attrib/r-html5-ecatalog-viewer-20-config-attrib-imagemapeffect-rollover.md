---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5eb17d-668a-4ad8-9f84-5684941d450d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 3%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

`[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>指定何时显示信息面板。 </p> <p>如果设置为<span class="codeph"> 1</span>，则当鼠标进入图像映射区域（如果图像映射具有非空的<span class="codeph"> rollover_key</span>属性）时，将显示信息面板。 </p> <p>如果设置为<span class="codeph">，则在选择图像映射时触发了0</span>信息面板（如果图像映射具有非空<span class="codeph"> rollover_key</span>和空<span class="codeph"> href</span>属性）。 </p> <p> 在触控设备（包括支持触控的桌面系统）上忽略，并自动设置为<span class="codeph"> 0</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-ccfedc2da28f412a86d03f390db92b4b}

可选.

## 默认 {#section-79eb39c444814c9398df1f5f3730d289}

`0`

## 示例 {#section-b548ed09b52b4b65888ac891af08d725}

`rollover=1`
