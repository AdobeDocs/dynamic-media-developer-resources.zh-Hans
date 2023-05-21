---
title: 作用中工作
description: 在伺服器上執行的工作。 此外，它也是排程工作的執行個體。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3d878207-99e4-4c75-ab12-b38a37c82fb7
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 8%

---

# [!DNL ActiveJob]{#activejob}

在伺服器上執行的工作。 此外，它也是排程工作的執行個體。

工作分為三種狀態：

* 已排定執行。
* 目前正在執行。
* 已完成執行（且已將資訊寫入工作記錄檔）。

若要傳回工作型別，請指定工作型別值。 您可以傳回下列工作：

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublish`
* `JobUploadDirectoryJob`
* `uploadUrlsJob`

## 参数 {#section-6590fe864a434000822b9ec384784512}

<table id="table_1C4DDAB4EB1341FDA92B6F14E0132F75"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 處理公司。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 處理工作。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 工作的唯一名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 原始名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">的原始名稱 <span class="codeph"> 作用中工作</span> 與工作一起提交的型別。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 系統傳回的工作型別選擇。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> state</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 系統傳回的使用中工作狀態選擇。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 排程工作之使用者的電子郵件地址。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">工作記錄檔詳細資料和電子郵件本地化的地區設定。 <p>指定地區設定為 <span class="codeph"> &lt;language_code&gt;[-&lt;country_code&gt;]</span>，其中語言程式碼為ISO-639所指定的小寫雙字母程式碼，而選用國家/地區程式碼為ISO-3166所指定的大寫雙字母程式碼。 例如，英文（美國）的地區設定字串將是： <span class="codeph"> en-US</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 說明</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">原本指定的工作說明 <span class="codeph"> submitjob</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 執行工作的伺服器名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> startDate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：dateTime</span> </td> 
   <td colname="col3"> 作用中工作的日期、時間和時區。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> totalSize</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 作用中工作的總大小。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 進度</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 工作進度（即工作接近完成的程度）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 說明工作進度的文字訊息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：dateTime</span> </td> 
   <td colname="col3"> 上次進度更新的日期、時間和時區。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskProgressArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：TaskProgressArray</span> </td> 
   <td colname="col3"> 非同步工作進度資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ImageServingPublishJob</span> </td> 
   <td colname="col3"> 影像伺服發佈工作的工作詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingRenderJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ImageServingRenderJob</span> </td> 
   <td colname="col3"> 影像演算發佈工作的工作詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videopublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：VideoPublishJob</span> </td> 
   <td colname="col3"> 視訊發佈工作的工作詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ImageServingPublishJob</span> </td> 
   <td colname="col3"> 伺服器目錄發佈工作的工作詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：UploadUrlsJob</span> </td> 
   <td colname="col3"> 上傳URL工作的工作詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：RipPdfJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：重新處理資產工作</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadPostJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：UploadPostJob</span> </td> 
   <td colname="col3"> 工作詳細資料，追蹤案頭上傳。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ExportJob</span> </td> 
   <td colname="col3">允許授權匯出先前上傳的檔案。 另請參閱 <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-exportjob.html" format="http" scope="external"> 匯出工作</a>. </td> 
  </tr> 
 </tbody> 
</table>
