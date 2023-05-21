---
title: icc
description: 輸出色彩設定檔。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---

# icc{#icc}

輸出色彩設定檔。

icc= *`profile`*[， *`renderIntent`*[，*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 設定檔</span></span> </p></td> 
  <td class="stentry"> <p>ICC色彩設定檔。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent </span> </span> </p></td> 
  <td class="stentry"> <p>可感知 |相對 |飽和度 |絕對 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1代表啟用，0代表停用黑點補償。 </p></td> 
 </tr> 
</table>

*`profile`* 指定呈現影像與工作設定檔不同時應該轉換到的輸出色域設定檔。 *`profile`* 必須為有效的 `icc::Name` 影像目錄或預設目錄的ICC設定檔對映中定義，或設定檔檔案的相對路徑(通常使用 [!DNL `.icc`] 或 [!DNL `.icm`] 字尾)。

>[!NOTE]
>
>*`profile`* 不可包含&#39;，&#39;字元，即使HTTP編碼亦然。

*`renderIntent`* 允許覆寫預設的色彩演算比對方式。

*`blackpointComp`* 如果輸出設定檔支援此功能，則啟用黑點補償。

>[!NOTE]
>
>並非所有的色彩轉換都支援所有 *`renderIntent`* 和 *`blackpointComp`* 選項。 通常，這些設定僅在ICC輸出設定檔代表印表機或監視器等輸出裝置時採用。 此外，有些ICC輸出設定檔不支援所有 *`renderIntent`* 選項。

## 屬性 {#section-b4042623a8ea40248c11b2153e5906b1}

可能發生在請求中的任何位置。 如果指定影像型別，則會傳回錯誤 `fmt=` 不符合 *`profile`*.

兩者 *`renderIntent`* 和 *`blackpointComp`* 若與指定的ICC設定檔不相容，則會被忽略。

CMYK輸出裝置設定檔較可能支援不同的演算意圖。

## 默认 {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

如果已啟用色彩管理且 `icc=` 未指定，伺服器會傳送已轉換為輸出設定檔的影像( `attribute::IccProfile*`)符合指定的影像型別 `fmt=`.

若未指定， *`renderIntent`* 繼承自 `attribute::IccRenderIntent`、和 *`blackpointComp`* 繼承自 `attribute::IccBlackPointCompensation`.

## 另请参阅 {#section-37ef83149fd74345956a98f633cc0294}

[色彩管理](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d)， [attribute：：IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127)， [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)， [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)， [attribute：：IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)， [屬性：：IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
