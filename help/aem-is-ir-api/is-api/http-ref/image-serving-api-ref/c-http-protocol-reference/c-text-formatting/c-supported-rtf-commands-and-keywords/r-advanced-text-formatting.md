---
description: 使用下列命令設定進階文字格式。
solution: Experience Manager
title: 進階文字格式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---

# 進階文字格式{#advanced-text-formatting}

使用下列命令設定進階文字格式。

<table id="table_43B2EB887C0F471BB60C23B570E7D3D2"> 
 <thead> 
  <tr> 
   <th class="entry"> 命令 </th> 
   <th class="entry"> 说明 </th> 
   <th class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \dn <span class="varname"> N </span> </span> </td> 
   <td> <p>下標而不變更字型大小。 </p> </td> 
   <td> <p>位置為半點；預設為6。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span> </span> </td> 
   <td> <p>不變更字型大小的上標。 </p> </td> 
   <td> <p>位置為半點；預設為6。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \字距微調 <span class="varname"> N </span> </span> </td> 
   <td> <p>以指定的字型大小停用/啟用。 </p> </td> 
   <td> <p>字型大小為半點，超過此點可套用字距微調；0表示停用字距微調；預設為1，表示所有字型大小都超過1/2點。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptical </span> </td> 
   <td> <p>選取視覺字距微調。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅限。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric </span> </td> 
   <td> <p>選取量度字距微調。 </p> </td> 
   <td> <p>默认. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd <span class="varname"> N </span> </span> </td> 
   <td> <p>修改字元間距。 </p> </td> 
   <td> <p>正或負的四分之一點；預設為0。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span> </span> </td> 
   <td> <p>修改字元間距。 </p> </td> 
   <td> <p>正或負兩週。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span> </span> </td> 
   <td> <p>水準字元縮放。 </p> </td> 
   <td> <p>正或負百分比；預設為100。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> N </span> </span> </td> 
   <td> <p>垂直字元縮放。 </p> </td> 
   <td> <p>正或負百分比；預設為100；Dynamic Media擴充功能。 </p> <p> <span class="codeph"> \charscaley </span> 也會在套用時縮放行距 <span class="codeph"> text= </span>. <span class="codeph"> textPs= </span> 無論垂直字元縮放多少，一律保留行距。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>選取由左至右的字元流程。 </p> </td> 
   <td> <p>默认. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>選取由右至左的字元流程。 </p> </td> 
   <td> <p> <span class="codeph"> text= </span> 僅限。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \組排文字 <span class="varname"> N </span> </span> </td> 
   <td> <p>啟用複製彎管頭並設定允許的最大字型大小。 </p> </td> 
   <td> <p>以半點為單位的字型大小； <span class="codeph"> textPs= </span> 僅限；Dynamic Media擴充功能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \複製管線 <span class="varname"> N </span> </span> </td> 
   <td> <p>最大複製配合線（軟限制）。 </p> </td> 
   <td> <p>0表示無行限制； <span class="codeph"> textPs= </span> 僅限；Dynamic Media擴充功能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span> </span> </td> 
   <td> <p>最大複製符合行數（截斷）。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅限；Dynamic Media擴充功能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span> </span> </td> 
   <td> <p>字元方向。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 僅限；非Roman字型會略過；在下列情況下會略過 <span class="codeph"> \stextflow1 </span> 未生效。 </p> <p>0垂直（預設）。 </p> <p>1順時針旋轉90度。 </p> </td> 
  </tr> 
 </tbody> 
</table>
