---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
source-git-commit: fd3a1fe47da5ba26b53ea9414bfec1e4c11d7392
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>指定何時顯示資訊面板。 </p> <p>若設為 <span class="codeph"> 1</span>時，當滑鼠進入影像地圖區域時會顯示資訊面板(如果影像地圖非空白， <span class="codeph"> rollover_key</span> 屬性)。 </p> <p>若設為 <span class="codeph"> 0</span> 選取影像地圖時會觸發資訊面板（如果影像地圖為非空白） <span class="codeph"> rollover_key</span> 和空白 <span class="codeph"> href</span> 屬性)。 </p> <p> 在觸控裝置（包括觸控式桌上型系統）上忽略，並自動設為 <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-ccfedc2da28f412a86d03f390db92b4b}

可选.

## 默认 {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## 示例 {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
