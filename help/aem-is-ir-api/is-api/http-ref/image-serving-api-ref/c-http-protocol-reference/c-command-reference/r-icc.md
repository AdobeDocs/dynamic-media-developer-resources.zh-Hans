---
description: 输出颜色配置文件.
solution: Experience Manager
title: icc
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 3%

---

# icc{#icc}

输出颜色配置文件.

`icc= *`物件`*[, *`renderIntent`*[, *`blackpointComp`*[, *`遞色`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 物件</span> </span> </p></td> 
  <td class="stentry"> <p>ICC色彩設定檔。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 可感知|相對|飽和度|絕對</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1代表啟用，0代表停用黑點補償。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 遞色</span></span> </p></td> 
  <td class="stentry"> <p>1代表啟用，0代表停用遞色。 </p></td> 
 </tr> 
</table>

*`object`* 指定與正在處理的設定檔不同時，影像應轉換到的輸出色域設定檔。 *`profile`* 必須為有效的 `icc::Name` 影像目錄或預設目錄的ICC設定檔對映中定義，或設定檔檔案的相對路徑(通常使用 [!DNL .icc] 或 [!DNL .icm] 字尾)。 另請參閱 [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)以取得其他資訊。

>[!NOTE]
>
>*`object`* 不可包含&#39;，&#39;字元，即使HTTP編碼亦然。

*`renderIntent`* 允許覆寫預設的色彩演算比對方式。

*`blackpointComp`* 如果輸出設定檔支援此功能，則會啟用黑點補償。

>[!NOTE]
>
>並非所有的色彩轉換都支援所有 *`renderIntent`* 和 *`blackpointComp`* 選項。 通常，這些設定僅在ICC輸出設定檔代表印表機或監視器等輸出裝置時採用。 此外，有些ICC輸出設定檔不支援所有 *`renderIntent`* 選項。

注意

*`dither`* 啟用遞色（實際上是誤差擴散），可避免或減少色階誤差。

## 屬性 {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

要求屬性。 如果指定影像型別，伺服器將傳回錯誤 `fmt=` 不匹配 *`profile`*.

*`renderIntent`* 和 *`blackpointComp`* 若與指定的ICC設定檔不相容，則會被忽略。 CMYK輸出裝置設定檔較可能支援不同的演算意圖。

## 默认 {#section-0b9fe2eb428447df8ae9948f11ab5aae}

如果已啟用色彩管理且 `icc=` 未指定，伺服器會傳遞已轉換為輸出設定檔的影像( `attribute::IccProfile*`)符合指定的影像型別 `fmt=`.

若未指定， *`renderIntent`* 繼承自 `attribute::IccRenderIntent`， *`blackpointComp`* 繼承自 `attribute::IccBlackPointCompensation`、和 *`dither`* 繼承自 `attribute::IccDither`.

## 另请参阅 {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute：：IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) ， [attribute：：IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)， [屬性：：IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)， [attribute：：IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)， [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)， [物件](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)， [色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)， [ICC設定檔對應參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)， [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
