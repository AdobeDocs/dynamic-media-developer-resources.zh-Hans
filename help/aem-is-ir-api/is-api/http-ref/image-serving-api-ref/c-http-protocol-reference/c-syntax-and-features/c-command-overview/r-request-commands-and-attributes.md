---
description: 無論這些命令在請求中出現的位置為何，都會套用這些命令。
solution: Experience Manager
title: 要求命令
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3f794f46-e7f0-4899-90fa-898a698dd629
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---

# 要求命令{#request-commands}

無論這些命令在請求中出現的位置為何，都會套用這些命令。

<table id="simpletable_3F7C17FB9E374EFDAD01EB24F57EC367"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> 快取</a> </p></td> 
  <td class="stentry"> <p>覆寫預設的回應快取行為。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2" type="reference" format="dita" scope="local"> 預設影像</a> </p></td> 
  <td class="stentry"> <p>指定要使用的影像，而非遺失的影像檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt</a> </p></td> 
  <td class="stentry"> <p>指定影像格式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517" type="reference" format="dita" scope="local"> icc</a> </p></td> 
  <td class="stentry"> <p>設定輸出色彩設定檔。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> iccEmbed</a> </p> </td> 
  <td class="stentry"> <p>將色彩設定檔嵌入回覆影像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed</a> </p></td> 
  <td class="stentry"> <p>將Photoshop路徑資料內嵌在回覆影像中。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed</a> </p></td> 
  <td class="stentry"> <p>將XMP中繼資料內嵌在回覆影像中。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-printres.md#reference-84f52afff4704c4b9d58e4bbbaea1491" type="reference" format="dita" scope="local"> printRes</a> </p> </td> 
  <td class="stentry"> <p>指定內嵌在回覆影像中的列印解析度值。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt</a> </p></td> 
  <td class="stentry"> <p>指定JPEG編碼屬性。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38" type="reference" format="dita" scope="local"> 量化</a> </p> </td> 
  <td class="stentry"> <p>指定GIF輸出的色彩量化屬性。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> 需要</a> </p></td> 
  <td class="stentry"> <p>選取請求型別。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md#reference-29a398cc59dc4caf9acd5f69c9ba9715" type="reference" format="dita" scope="local"> resMode</a> </p></td> 
  <td class="stentry"> <p>指定影像重新取樣或內插模式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14" type="reference" format="dita" scope="local"> 模板</a> </p> </td> 
  <td class="stentry"> <p>指定複合範本。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb" type="reference" format="dita" scope="local"> locale</a> </p></td> 
  <td class="stentry"> <p>指定複合範本。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id</a> </p> </td> 
  <td class="stentry"> <p>影像/中繼資料版本ID。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3" type="reference" format="dita" scope="local"> imageSet</a> </p> </td> 
  <td class="stentry"> <p>指定要用於此要求的影像集。 </p></td> 
 </tr> 
</table>
