---
title: 使用者介面元素的本地化
description: Video Viewer顯示的特定內容必須經過本地化，包括縮放按鈕和全熒幕按鈕。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: c386a09c-21ce-4105-b416-e6ae50219af0
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 使用者介面元素的本地化{#localization-of-user-interface-elements}

Video Viewer顯示的特定內容必須經過本地化，包括縮放按鈕和全熒幕按鈕。

檢視器中可本地化的每個文字內容，都會以稱為SYMBOL的特殊檢視器SDK識別碼表示。 任何SYMBOL都有英文地區設定的預設關聯文字值( `"en"`)隨現成可用的檢視器提供。 它也可以視需要為許多區域設定設定使用者定義的值。

當檢視器啟動時，它會檢查目前的地區設定，檢視地區設定的每個受支援的SYMBOL是否有使用者定義的值。 如果有的話，它會使用使用者定義的值；否則，會退回現成的預設文字。

使用者定義的本地化資料可作為本地化JSON物件傳遞至檢視器。 這類物件包含支援的語言環境清單、每個語言環境的SYMBOL文字值，以及預設語言環境。

以下是這類本地化物件的範例：

```
{ 
"en":{ 
"CloseButton.TOOLTIP":"Close", 
"ZoomInButton.TOOLTIP":"Zoom In" 
 }, 
 "fr":{ 
"CloseButton.TOOLTIP":"Fermer", 
"ZoomInButton.TOOLTIP":"Agrandir" 
}, 
defaultLocale:"en" 
}
```

在上述範例中，本地化物件會定義兩個地區設定( `"en"` 和 `"fr"`)並提供每個地區設定中兩個使用者介面元素的本地化。

網頁程式碼應將此類本地化物件傳遞至檢視器建構函式，當做值 `localizedTexts` 設定物件的欄位。 另一種選擇是呼叫 `setLocalizedTexts(localizationInfo)` 方法。

支援下列SYMBOL：

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>符號 </p> </th> 
   <th colname="col2" class="entry"> <p>工具提示…… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>頂層檢視器元素的ARIA標籤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>主要檢視元件的ARIA角色說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>鍵盤使用者的ARIA使用提示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>關閉按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>放大顯示按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>縮小顯示按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>縮放重設按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>正常狀態下的全熒幕按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>全熒幕狀態的全熒幕按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>向左捲動按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>向右捲動按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>向上捲動按鈕。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>向下捲動按鈕。 </p> </td> 
  </tr> 
 </tbody> 
</table>
