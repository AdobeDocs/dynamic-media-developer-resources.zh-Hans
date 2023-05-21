---
title: 鍵盤協助工具與導覽
description: 可使用鍵盤存取Basic Zoom、eCatalog、eCatalog Search、Flyout、Inline Zoom、Mixed Media、Spin、Video、Zoom、Dimension (3D)、Carousel、Interactive Image、Interactive Video和Video360檢視器介面中公開的所有功能。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# 鍵盤協助工具與導覽{#keyboard-accessibility-and-navigation}

可使用鍵盤存取Basic Zoom、eCatalog、eCatalog Search、Flyout、Inline Zoom、Mixed Media、Spin、Video、Zoom、Carousel、Dimensional (3D)、互動式影像、互動式視訊和Video360檢視器介面中公開的所有功能。

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## 鍵盤協助工具與導覽 {#topic-f5650e9493404e55a3627c8d1366b861}

可使用鍵盤存取Basic Zoom、eCatalog、eCatalog Search、Flyout、Inline Zoom、Mixed Media、Spin、Video、Zoom、Carousel、Dimensional (3D)、互動式影像、互動式視訊和Video360檢視器介面中公開的所有功能。

一般使用者可以使用以下工具在檢視器使用者介面元素之間導覽： **[!UICONTROL 標籤]** 和 **[!UICONTROL Shift+Tab鍵]** 按鍵動作。 使用 **[!UICONTROL 標籤]** 將輸入焦點推進至Tab鍵瀏覽順序中的下一個使用者介面元素；使用 **[!UICONTROL Shift+Tab鍵]** 將輸入焦點帶回上一個使用者介面元素。 焦點周遊會依循熒幕上的自然使用者介面元素位置，並依序由左至右、由上至下的順序移動。

根據作業系統和網頁瀏覽器設定，具有輸入焦點的使用者介面元素會收到視覺焦點指示。 例如，視覺指示器可以是圍繞使用者介面元素呈現的細邊框。

您可以在檢視器CSS中停用或自訂這類焦點反白顯示。 在此「說明」系統的目錄下，以特定的檢視器名稱（例如「基本縮放」或「互動式視訊」）按一下 **自訂 *檢視器名稱*** >**&#x200B;焦點反白顯示&#x200B;**.

個別檢視器使用者介面元素所支援的按鍵在多數情況下是顯而易見的且易於發現。

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>操作 </p> </th> 
   <th colname="col2" class="entry"> <p>擊鍵 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>啟動按鈕元件 </p> </td> 
   <td colname="col2"> <p>空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>放大或縮小 </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> 或 <span class="uicontrol"> - </span>（分別）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>縮放重設 </p> </td> 
   <td colname="col2"> <p>Esc金鑰。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>平移 </p> </td> 
   <td colname="col2"> <p>向上、向下、向左或向右鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>旋轉360度影像 </p> </td> 
   <td colname="col2"> <p>當影像處於重設狀態時，請使用方向鍵。 </p> <p>使用多維度迴轉集時，請使用向上鍵或向下鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>產品色票選擇 </p> </td> 
   <td colname="col2"> <p>向上、向下、向左或向右方向鍵；Home或End鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>產品色票啟用 </p> </td> 
   <td colname="col2"> <p>空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊與互動式視訊，逐步倒帶 </p> </td> 
   <td colname="col2"> <p>向左鍵或向上鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊與互動式視訊，快速前進 </p> </td> 
   <td colname="col2"> <p>向右鍵或向下鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊和互動式視訊，移至開頭或結尾 </p> </td> 
   <td colname="col2"> <p>Home鍵或End鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊和互動式視訊，當焦點位於滑杆上時控制音量等級 </p> </td> 
   <td colname="col2"> <p>向上、向下、向左或向右方向鍵；Home或End鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊與互動式視訊、可變動音量 </p> </td> 
   <td colname="col2"> <p>當焦點在其滑桿零件上時，可控制音量等級的「箭頭」、「首頁」和「結束」鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>視訊，當顯示強制回應對話方塊時，焦點周遊會變成僅限於對話方塊控制項。 </p> </td> 
   <td colname="col2"> <p>按Esc鍵關閉對話方塊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>輪播，在主檢視中變更橫幅影像 </p> </td> 
   <td colname="col2"> <p>向左或向右鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>輪播、熱點選擇和熱點啟用 </p> </td> 
   <td colname="col2"> <p>熱點選擇：向上、向下、向左或向右方向鍵 </p> <p>熱點啟動：空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，在主檢視中變更頁面影像 </p> </td> 
   <td colname="col2"> <p> 向左鍵或向右鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，縮圖選取範圍 </p> </td> 
   <td colname="col2"> <p>方向鍵；Home和End鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，色票啟用 </p> </td> 
   <td colname="col2"> <p>空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，熱點選取 </p> </td> 
   <td colname="col2"> <p>方向鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，啟用 </p> </td> 
   <td colname="col2"> <p>空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，啟用下拉式元件 </p> </td> 
   <td colname="col2"> <p> 向下鍵、空格鍵或Enter鍵。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog，焦點在下拉面板時 </p> </td> 
   <td colname="col2"> <p>使用方向鍵在啟動前選取面板中的特定專案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog顯示強制回應對話方塊時，焦點周遊會變成僅限對話方塊控制項。 </p> </td> 
   <td colname="col2"> <p>按Esc鍵關閉對話方塊。 </p> </td> 
  </tr> 
 </tbody> 
</table>
