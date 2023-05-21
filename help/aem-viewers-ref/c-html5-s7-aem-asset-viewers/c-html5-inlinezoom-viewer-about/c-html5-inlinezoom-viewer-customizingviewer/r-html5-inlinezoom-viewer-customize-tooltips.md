---
title: 工具提示
description: 在案頭系統上，某些使用者介面元素（如按鈕）具有在滑鼠懸停時顯示的工具提示。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: bcbdd047-428b-48f8-9bd9-600f36f2e0b7
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# 工具提示{#tooltips}

在案頭系統上，某些使用者介面元素（如按鈕）具有在滑鼠懸停時顯示的工具提示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主要檢視器區域的CSS屬性**

工具提示的外觀由下列CSS類別選取器控制：

```
.s7tooltip
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
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> 背景邊框半徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p> 背景邊框顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 背景颜色. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>文字色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>文字字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>文字字型大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>如果工具提示樣式是從內嵌網頁中自訂的，則所有屬性都必須包含 `!IMPORTANT` 規則。 不過，如果工具提示是在檢視器的CSS檔案中自訂的，則不需要使用。

範例 — 若要設定工具提示，該工具提示的灰色邊框具有3畫素圓角半徑、黑色背景和使用Arial® 11畫素大小寫入的白色文字：

```
.s7tooltip { 
 border-radius: 3px 3px 3px 3px; 
 border-color: #999999; 
 background-color: #000000; 
 color: #FFFFFF; 
 font-family: Arial, Helvetica, sans-serif; 
 font-size: 11px; 
}
```
