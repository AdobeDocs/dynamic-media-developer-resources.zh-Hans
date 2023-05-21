---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 19239fa8-65a8-487f-9370-42bb93d862d5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 4%

---

# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`时段`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幻燈片|翻轉|自動</span> </p> </td> 
   <td colname="col2"> <p> 指定套用至影格變更的效果型別。 </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> 幻燈片</span> 啟動一個轉變，舊框架滑出檢視，新框架滑入檢視。 </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> 翻轉</span> 當使用者可以拖曳四個跨頁角之一并執行互動式頁面翻轉時，啟用頁面翻轉效果。 </p> <p>時間 <span class="codeph"> 翻轉</span> 使用，元件的外觀由控制 <span class="codeph"> pageturnstyle</span> 修飾元與 <span class="codeph"> .s7pagedider</span> 已忽略CSS類別。 </p> <p>注意︰  <p><span class="codeph"> 翻轉</span> Motorola Xoom不支援動畫。 </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> 自動</span> 設定桌上型電腦系統上的旋轉影格切換，以及觸控裝置上的投影片切換。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 时段</span></span> </p> </td> 
   <td colname="col2"> <p>指定持續時間（以秒為單位） <span class="codeph"> 幻燈片</span> 或 <span class="codeph"> 翻轉</span> 切換效果。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-4d25a3f483834d2b9586fa70270ce6bd}

可选.

## 默认 {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## 示例 {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
