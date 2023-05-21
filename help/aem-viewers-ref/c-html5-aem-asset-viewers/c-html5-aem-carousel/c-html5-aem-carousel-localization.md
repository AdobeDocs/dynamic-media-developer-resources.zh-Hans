---
title: 使用者介面元素的本地化
description: 「轉盤檢視器」顯示的某些內容必須經過本地化。 此內容包含幻燈片導覽按鈕。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 05f5abe0-1124-4114-864d-440699bcdc39
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# 使用者介面元素的本地化{#localization-of-user-interface-elements}

「轉盤檢視器」顯示的某些內容必須經過本地化。 此內容包含幻燈片導覽按鈕。

檢視器中可本地化的每個文字內容，都會以稱為SYMBOL的特殊檢視器SDK識別碼表示。 任何SYMBOL都有預設的英文地區設定相關文字值( `"en"`)隨附立即可用的檢視器，而且可能視需要為許多語言環境設定使用者定義的值。

當檢視器啟動時，它會檢查目前的地區設定，檢視此類地區設定的每個受支援的SYMBOL是否有使用者定義的值。 如果有的話，它會使用使用者定義的值；否則，會退回現成的預設文字。

使用者定義的本地化資料可作為本地化JSON物件傳遞至檢視器。 這類物件包含支援的語言環境清單、每個語言環境的SYMBOL文字值，以及預設語言環境。

以下是這類本地化物件的範例：

```
{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left", 
"PanRightButton.TOOLTIP":"Right" 
 }, 
 "fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste", 
"PanRightButton .TOOLTIP":"Droit" 
}, 
defaultLocale:"en" 
}
```

在上述範例中，本地化物件會定義兩個地區設定( `"en"` 和 `"fr"`)並提供每個地區設定中兩個使用者介面元素的本地化。

網頁程式碼應將本地化物件傳遞至檢視器建構函式，其值為 `localizedTexts` 設定物件的欄位。 另一種選擇是呼叫，傳遞本地化物件 `setLocalizedTexts(localizationInfo)` 方法。

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
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>選取的播放暫停按鈕狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>未選取的播放暫停按鈕狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELEVIEWER_TOOLTIP_GOTO </span> </p> </td> 
   <td colname="col2"> <p> 上一張和下一張投影片按鈕的工具提示和ARIA標籤。 </p> <p>接受兩個取代Token： <span class="codeph"> $CURRENT_FRAME$ </span> 目前投影片索引和 <span class="codeph"> $TOTAL_FRAMES$ </span> 以取得投影片總數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p> 頂層檢視器元素的ARIA標籤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p> 主要檢視元件的ARIA角色說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p> 鍵盤使用者的ARIA使用提示。 </p> </td> 
  </tr> 
 </tbody> 
</table>
