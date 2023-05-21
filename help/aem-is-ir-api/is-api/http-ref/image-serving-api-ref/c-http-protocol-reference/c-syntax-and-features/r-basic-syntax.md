---
description: HTTP通訊協定基本語法如下。
solution: Experience Manager
title: 影像伺服HTTP通訊協定基本語法
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---

# 影像伺服HTTP通訊協定基本語法{#image-serving-http-protocol-basic-syntax}

HTTP通訊協定基本語法如下：

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 請求</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> 伺服器</span>/is/image[/<span class="varname"> 物件</span>][？<span class="varname"> 修飾元</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 伺服器 </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[：<span class="varname"> 連線埠</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 物件</span> </span> </p></td> 
  <td class="stentry"> <p>來源物件規範（影像路徑或影像目錄專案）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修飾元</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修飾元</span>*[&amp;<span class="varname"> 修飾元</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修飾元</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">命令|{$<span class="varname"> 巨集</span>$}|{.<span class="varname"> 評論</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 命令</span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}}[=<span class="varname"> 值</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 巨集</span> </span> </p> </td> 
  <td class="stentry"> <p>命令巨集的名稱。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 評論</span> </span> </p></td> 
  <td class="stentry"> <p>註解字串（被伺服器忽略）。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>支援的命令或屬性名稱之一。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>自訂變數的名稱。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 值</span> </span> </p></td> 
  <td class="stentry"> <p>命令或變數值。 </p></td> 
 </tr> 
</table>

*`server_address`*， *`cmdName`*， *`macro`*、和 *`var`* 不區分大小寫。 伺服器會保留所有其他字串值的大小寫。

*`value`* 是命令專用的，可由一或多個以逗號分隔的值組成。 如需詳細資訊，請參閱個別命令的說明。

## 伺服器識別碼 {#section-926ae55ddba14b8d952147a5fd701e14}

此 [!DNL /is/image] 所有「影像伺服」的HTTP請求都需要根上下文。

## HTTP解碼 {#section-20922baccd804d2d986b44ce9a183a7d}

影像伺服首次擷取 *`object`* 和 *`modifiers`* 來自傳入的要求。 *`object`* 然後會分隔成路徑元素，這些元素會個別進行HTTP解碼。 此 *`modifiers`* 字串分隔為 *`command`*= *`value`* 配對，和 *`value`* 然後在命令特定處理之前進行HTTP解碼。

>[!NOTE]
>
>除非檔案另有說明，否則所有不安全的字元都必須按照HTTP標準編碼。 如需詳細資訊，請參閱HTTP規格。

## 注释 {#section-69ef0be0f17a418c87a0eba21c2ddb00}

註解可內嵌於任何位置的請求字串中，並以period(.)識別 緊接在命令分隔符號(&amp;)後面。 註解會在下次出現（未編碼）命令分隔符號時終止。 此功能可用來新增資訊至不供「影像伺服」使用的請求，例如時間戳記和資料庫ID。

## 另请参阅 {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[資料型別](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa)， [HTTP/1.1規格](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
