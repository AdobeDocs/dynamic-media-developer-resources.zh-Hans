---
description: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2669c8e2-c942-420f-8262-9d76d5c499a2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

[!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *`分隔線寬度`*, *`分隔線色彩`*, *`分隔線不透明度`*, *`borderOnOff`*, *`borderColor`*, *`fillColor`*`]

控制元件外觀，當 [!DNL `PageView.frametransition`] 設為 [!DNL `turn`] 或 [!DNL `auto`] 在桌上型電腦系統上。

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 分隔線寬度</span></span> </p> </td> 
   <td colname="col2"> <p> 分隔跨頁左右頁面的頁面分隔線陰影寬度（畫素）。 它也會控制車削頁面旁邊所顯示的執行陰影寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 分隔線不透明度</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB格式的陰影顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 分隔線不透明度</span></span> </p> </td> 
   <td colname="col2"> <p>範圍中的陰影不透明度 <span class="codeph"> 0</span> 至 <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> 標幟(可 <span class="codeph"> 0</span> 或 <span class="codeph"> 1</span>)會開啟和關閉開啟頁面周圍的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB格式的邊框顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> 翻頁動畫期間使用的元件區域的純色填滿色彩，以RRGGBB格式顯示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-54c634116cfe4f17813318e07539264c}

可选.

## 默认 {#section-43fd13f639c2480c82658fafeeaf0846}

[!DNL `40,909090,1,1,909090,FFFFFF`]

## 示例 {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`]
