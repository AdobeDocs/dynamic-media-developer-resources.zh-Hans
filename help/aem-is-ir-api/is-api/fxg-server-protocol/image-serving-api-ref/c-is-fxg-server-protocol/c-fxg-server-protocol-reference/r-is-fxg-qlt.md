---
description: Jpeg品質。 指定JPEG編碼屬性來控制壓縮等級。 這進而會改變檔案大小（回覆資料量），並間接改變結果影像的視覺品質。
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 15%

---

# qlt{#qlt}

Jpeg品質。 指定JPEG編碼屬性來控制壓縮等級。 這進而會改變檔案大小（回覆資料量），並間接改變結果影像的視覺品質。

` qlt= *`品質`*[, *`色度`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 品質 </span> </span> </p> </td> 
  <td class="stentry"> <p>編碼品質JPEG(1...100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 色度 </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度縮減取樣（0=一般，1=停用）；選擇性，預設為0。 </p> </td> 
 </tr> 
</table>

僅在以下情況下使用： `fmt=jpg`. 已忽略，否則

高品质值可增大文件并提升品质，低品质值可减小文件并降低可感知的图像品质。如果值大于 90，所产生的图像往往与未解压缩图像几乎没有区别。

設定 `chroma` 此旗標可停用典型RGB編碼器所採用的JPEG色度縮減取樣。 當邊緣是由色相變化而不是亮度所定義時，這可能會增加影像中邊緣的感知銳利度。 設定此旗標可能會導致檔案大小稍微增加。 如果文字看起來有點模糊，請嘗試使用此設定。

`chroma` 如果輸出畫素型別為CMYK或灰色，則會被忽略。

## 示例 {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
