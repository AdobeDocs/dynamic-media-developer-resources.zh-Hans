---
description: 方向
solution: Experience Manager
title: 方向
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 3%

---

# 方向{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>指定頁面在主檢視和縮圖中的顯示方式。 它也會指定使用者與檢視器使用者介面的互動方式，以便在目錄框架之間變更。 </p> <p>時間 <span class="codeph"> left </span> 使用「 」時，它會設定初始頁面的靠右對齊方式，以及最後一頁的靠左對齊方式。 它會依由左至右的轉譯順序來拼接個別頁面子影像。 它也會將主檢視設定為使用從右至左的投影片動畫來推進目錄(如果是 <span class="codeph"> PageView.frametransition </span> 設為滑動)。 最後，縮圖會設定為由左至右的填入順序。 </p> <p>同樣地，當 <span class="codeph"> 右側 </span> 使用「 」時，它會設定初始頁面的左對齊方式，以及最後一頁的右對齊方式。 它會依由右至左的轉譯順序來拼接個別頁面子影像。 它也會設定主檢視，以使用由左至右的投影片動畫來推進目錄(如果是 <span class="codeph"> PageView.frametransition </span> 設為滑動)。 最後，它會反轉縮圖順序，讓縮圖檢視以由右至左、由上至下的方向填入。 </p> <p>時間 <span class="codeph"> 自動 </span> 設定，則套用檢視器 <span class="codeph"> 右側 </span> locale設定為時的模式 <span class="codeph"> ja； </span>否則，它會使用 <span class="codeph"> left </span> 模式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-a66ce10d6c0b449883f654e7e0657e2c}

可选.

## 默认 {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## 示例 {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
