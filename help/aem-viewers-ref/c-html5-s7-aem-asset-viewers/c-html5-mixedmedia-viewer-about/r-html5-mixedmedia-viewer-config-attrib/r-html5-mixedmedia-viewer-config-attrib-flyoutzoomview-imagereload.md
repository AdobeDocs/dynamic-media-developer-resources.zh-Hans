---
title: FlyoutZoomView.imagereload
description: 設定在調整大小期間，元件如何擷取主檢視和彈出式檢視的新影像。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

設定在調整大小期間，元件如何擷取主檢視和彈出式檢視的新影像。

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`寬度`*[; *`寬度`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p>當設定為 <span class="codeph"> 0 </span>時，元件不會在調整大小期間載入新影像，而且彈出式檢視中的影像解析度不會變更。 </p> <p>當設定為 <span class="codeph"> 1 </span> 可讓您為載入至主檢視的影像指定一或多個寬度中斷點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 中斷點， <span class="varname"> 寬度 </span>[； <span class="varname"> 寬度 </span>] </span> </p> </td> 
   <td colname="col2"> <p>影像的寬度中斷點已載入主檢視。 元件一律使用最佳配合大小來初始負載。 在調整大小之後，它可確保下載主檢視中的影像時，寬度始終等於最接近的大型中斷點，並在使用者端上縮小比例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
