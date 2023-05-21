---
title: 縮放模式
description: 設定縮放互動的型別。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---

# 縮放模式{#zoommode}

設定縮放互動的型別。

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuous|inline|auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 連續 </span> 啟用傳統縮放，也就是當您在主檢視中按一下、點兩下或捏出時，影像會逐漸放大。 若要回到初始檢視，請縮小或重設縮放狀態。 類別 </p> <p> <span class="codeph"> 內嵌 </span> 啟用即時縮放，也就是當您將滑鼠懸停在桌上型電腦的主檢視上，或是觸控並按住觸控裝置時，會立即顯示縮放後的影像。 當您從檢視移動滑鼠或放開手指後，影像會自動回覆為初始狀態。 在 <span class="codeph"> 內嵌 </span> 模式，巢狀影像集會平面化並顯示為個別縮圖。 類別 <span class="codeph"> 自動 </span> 在桌上型電腦上啟用內嵌模式，在觸控裝置上啟用連續模式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
