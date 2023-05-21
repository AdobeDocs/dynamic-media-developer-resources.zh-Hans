---
title: initialframe
description: 所有檢視器通用的引數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 3%

---

# initialframe{#initialframe}

所有檢視器通用的引數。

>[!NOTE]
>
>這個命令不適用於Video Image Viewer。

` initialFrame= *`frameIdx`*[ *`，pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定檢視器在載入時顯示的從零開始的影格索引。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>當裝置為縱向方向時，跨頁中的頁面索引（從零開始）。 若為「由左至右」的環境， <span class="codeph"> 0</span> 表示「左側頁面」和 <span class="codeph"> 1</span> 表示「正確頁面」。 若是「由右至左」的環境，情況則相反： <span class="codeph"> 0</span> 表示「正確頁面」和 <span class="codeph"> 1</span> 表示「左側頁面」。 </p> <p>若未指定， <span class="codeph"> 0</span> 預設為使用。 當裝置為橫向時忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

可选.

## 默认 {#section-d411e450028c460392cb8508f8ccc5d9}

無預設值。

## 示例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
