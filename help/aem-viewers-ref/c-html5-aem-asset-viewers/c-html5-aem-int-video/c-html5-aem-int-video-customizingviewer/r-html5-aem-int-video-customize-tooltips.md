---
title: 工具提示
description: 在案頭系統上，某些使用者介面元素（例如按鈕）具有在滑鼠懸停時顯示的工具提示。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 430809d8-3d51-49b7-b6bf-c3c3c77501ff
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 3%

---

# 工具提示{#tooltips}

在案頭系統上，某些使用者介面元素（例如按鈕）具有在滑鼠懸停時顯示的工具提示。

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
>如果工具提示樣式是從內嵌網頁中自訂的，則所有屬性都必須包含 `!IMPORTANT` 規則。 如果在檢視器的CSS檔案中自訂工具提示，則不需要此備註。

## 示例 {#section-59e009fd05b14019936aba04d7ca779d}

若要設定具有灰色邊框的工具提示，該邊框具有三個畫素的圓角半徑、黑色背景，以及Arial® 11畫素的白色文字：

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
