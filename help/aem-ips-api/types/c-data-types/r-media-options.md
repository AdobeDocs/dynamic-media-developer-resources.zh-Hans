---
description: 為您的視訊產生縮圖影像。
solution: Experience Manager
title: MediaOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f37d935d-fe74-4878-8477-d2144d58d982
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 7%

---

# [!DNL MediaOptions]{#mediaoptions}

為您的視訊產生縮圖影像。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoEncodingPresetsArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：HandleArray</span> </td> 
   <td colname="col3">陣列 <span class="codeph"> 屬性集</span> 處理參考視訊編碼預設集以轉碼視訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generateThumbnail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 為true時，會擷取視訊的第一個影格，並當做縮圖影像使用。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailoptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ThumbnailOptions</span> </td> 
   <td colname="col3">可选. 可讓您選擇特定的視訊影格做為縮圖影像。 <p>若要指定縮圖影像，請為您要使用的影格傳入時間（從視訊開始算起的毫秒）。 值範圍從0到視訊結尾。 <p>注意：如果您不正確指定時間， <span class="codeph"> generateThumbnail</span> 預設為true。 </p></p><p>另請參閱 <a href="../../types/c-data-types/r-thumbnail-options.md#reference-370088b0a4ce4096b9b3e5489a368b5c" format="dita" scope="local"> 縮圖選項</a>. </p></td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-a9356de782d74af6933c39fa7ad12212}

```
<complexType name="MediaOptions">
        <sequence>
            <element name="videoEncodingPresetsArray" type="types:HandleArray" minOccurs="0"/>
            <element name="generateThumbnail" type="xsd:boolean" minOccurs="0"/>
            <element name="thumbnailOptions" type="types:ThumbnailOptions" minOccurs="0"/>
        </sequence>
    </complexType>
```

## 使用者 {#section-87cb83407198432c95eaa2db9f12f9db}

此 `mediaOptions` 型別使用者：

* [UploadDirectory作業](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadpostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadURLsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
