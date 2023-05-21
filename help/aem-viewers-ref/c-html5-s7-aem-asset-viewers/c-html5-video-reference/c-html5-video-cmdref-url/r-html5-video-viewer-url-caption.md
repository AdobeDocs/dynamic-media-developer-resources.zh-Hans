---
title: 註解
description: Video Viewer的URL命令。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: a9af3335-ae18-4399-9014-47ec0306a087
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 8%

---

# 註解{#caption}

Video Viewer的URL命令。

` caption= *`文件`*[,0|1]`

檢視器透過託管的WebVTT檔案支援隱藏式字幕。 不支援重疊的提示和區域。 支援的提示定位運運算元包括：

<table id="table_62D89A06EC9E4E7983D1F26A2C85A621"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>鍵 </p> </th> 
   <th colname="col2" class="entry"> <p>名称 </p> </th> 
   <th colname="col3" class="entry"> <p>值 </p> </th> 
   <th colname="col4" class="entry"> <p>说明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> A </p> </td> 
   <td colname="col2"> <p>文字對齊 </p> </td> 
   <td colname="col3"> <p><span class="codeph"> left|right|middle|start|end</span> </p> </td> 
   <td colname="col4"> <p> 控制文字對齊方式。 </p> <p>預設為 <span class="codeph"> 中間</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>文字位置 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 註解文字開頭內嵌至VideoPlayer元件的百分比。 </p> <p>預設值為0%。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>行大小 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 用於註解的視訊寬度百分比。 </p> <p>預設為100%。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>行位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整數 </p> </td> 
   <td colname="col4"> <p> 決定頁面上的行位置。 </p> <p>如果以整數表示（無百分比符號），則為文字顯示位置上方的行數。 </p> <p>如果它是百分比（百分比符號是最後一個字元），則註解文字會在顯示區域顯示這個百分比值。 </p> <p>預設為100%。 </p> </td> 
  </tr> 
 </tbody> 
</table>

不支援WebVTT檔案中存在的其他WebVTT功能，但不應中斷字幕。

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 文件</span></span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT標題內容的URL或路徑。 透過ImageServing提供WebVTT檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 指定預設註解狀態(啟用為 <span class="codeph"> 1</span>)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

无。

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
