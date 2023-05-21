---
title: ErrorDetail
description: 錯誤訊息詳細資料。 指定透過HTTP傳回之錯誤訊息的詳細資訊層級為error.message值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39d7fc44-7605-4f93-b2f9-0a6e8bc76ec7
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---

# ErrorDetail{#errordetail}

錯誤訊息詳細資料。 指定透過HTTP傳回之錯誤訊息的詳細資訊層級為error.message值。

## 标题 {#section-c10d75d72ee24d16a67cc8d927f1deba}

允許使用下列值：

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>僅限標題。 傳回錯誤的簡短一般說明。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>簡短訊息。 保留以供日後使用。 目前傳回的資訊與0相同。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細訊息。 提供有關錯誤的使用者層級詳細資訊。 可能包含敏感資訊，例如檔案路徑。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完整的偵錯資訊。 在適用時新增Java™棧疊追蹤。 錯誤影像絕不包含棧疊追蹤，而是傳回第2級資訊 <span class="codeph"> $error.message</span>. </p></td> 
 </tr> 
</table>

* 對於可公開存取的即時伺服器，建議使用層級0。
* 建議將第2級用於中繼、品質保證和應用程式開發伺服器。
* 向Dynamic Media技術支援報告問題時，第3級資訊可能會很有用。

## 屬性 {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

列舉值，必須是0、1、2或3。

## 默认 {#section-5e78d550050840cc9a1de811c581b94f}

繼承自 `default::ErrorDetail` 若未指定或為空。

## 另请参阅 {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute：：ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
