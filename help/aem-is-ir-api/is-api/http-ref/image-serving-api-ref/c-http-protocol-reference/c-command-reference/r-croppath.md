---
description: 可讓您裁切至內嵌命名路徑的邊界方框。 此裁切作業進而會變更影像的大小。
solution: Experience Manager
title: cropPathE
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78e9f994-d638-49a7-ac42-3146e47210e3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# cropPathE{#croppathe}

可讓您裁切至內嵌命名路徑的邊界方框。 此裁切作業進而會變更影像的大小。

`cropPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>內嵌在圖層來源影像中的路徑名稱（僅限ASCII）。 </p> <p> <span class="codeph"><span class="varname"> pathName</span></span> 是內嵌在圖層來源影像中的路徑名稱。 路徑會視需要自動轉換，以維持與影像內容的相對對齊方式。 如果超過一個 <span class="codeph"><span class="varname"> pathName</span></span> 指定時，伺服器會裁切至每個路徑的邊界方框，一次一個。 任何 <span class="codeph"><span class="varname"> pathName</span></span> 在來源影像中找不到，則會被忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

圖層屬性。 套用至目前圖層或複合影像，如果 `layer=comp`. 被效果圖層忽略。

`cropPathE=` 如果在圖層來源影像中找不到具有指定名稱的路徑，或圖層來源不是影像，則會忽略該專案。

## 默认 {#section-d1986aa31af14767aeb1b4a57add67f4}

「無」，表示沒有額外的圖層裁切。

## 另请参阅 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[裁切](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab)， [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
