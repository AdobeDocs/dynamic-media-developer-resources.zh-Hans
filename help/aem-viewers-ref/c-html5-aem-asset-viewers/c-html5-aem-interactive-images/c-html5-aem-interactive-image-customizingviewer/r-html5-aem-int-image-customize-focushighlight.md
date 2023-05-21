---
title: 焦點反白顯示
description: 焦點檢視器UI元素周圍所顯示的輸入焦點反白顯示，是由CSS類別選取器所控制。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 89f34a96-2b21-4169-8c25-4b53005e59b8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# 焦點反白顯示{#focus-highlight}

焦點檢視器UI元素周圍所顯示的輸入焦點反白顯示，是由CSS類別選取器所控制。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS屬性**

外觀由下列CSS類別選取器控制：

```
.s7interactiveimage *:focus
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 大綱 </span> </p> </td> 
   <td colname="col2"> <p>焦點反白顯示樣式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要停用所有檢視器使用者介面元素的預設瀏覽器焦點反白顯示，請將下列CSS選取器新增至檢視器的樣式表：

```
.s7interactiveimage *:focus { 
 outline: none; 
}
```
