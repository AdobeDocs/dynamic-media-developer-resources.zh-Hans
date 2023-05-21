---
description: 將工作提交至系統。
solution: Experience Manager
title: submitjob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b1dc7a0e-da9a-4086-822b-5274bd62eadf
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 11%

---

# submitjob{#submitjob}

將工作提交至系統。

语法

## 授權的使用者型別 {#section-eb7024277bec43c79e03f396205be16f}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-31a07dbccf964850883e817384499459}

**輸入(submitJobParam)**

<table id="table_9CB1F668E036422E8CE4E0BBA42EC44C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名称 </p> </th> 
   <th colname="col2" class="entry"> <p>类型 </p> </th> 
   <th colname="col3" class="entry"> <p>必需 </p> </th> 
   <th colname="col4" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>公司控點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>對提交工作的使用者進行處理。 </p> <p> <p>注意：系統會傳送電子郵件給指定的使用者，指定者： <span class="codeph"> userHandle</span>. 若 <span class="codeph"> userHandle</span> 如果未提供，則提交工作的人員會收到電子郵件。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>作业名称. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>用於工作記錄檔詳細資料和電子郵件本地化的地區設定。 </p> <p>地區設定指定為 <span class="codeph"> &lt;language_code&gt;</span> 和 <span class="codeph"> [&lt;country_code&gt;]</span>，其中語言程式碼為ISO-639所指定的小寫雙字母程式碼，而選用國家/地區程式碼為ISO-3166所指定的大寫雙字母程式碼。 例如，英文（美國）的地區設定字串將是： en-US。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：dateTime</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>執行工作的日期和時間。 </p> <p>注意：提供請求的時區。 時區會調整為目標IPS伺服器的時區。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>決定何時執行工作。 </p> <p> 可以是 <span class="codeph"> cron</span> 重複執行作業的字串。 </p> <p>排程總是相對於伺服器的本機時區。 如需自訂排程格式，請參閱IPS檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 說明</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>工作說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ExportJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>匯出先前上載的檔案。 </p> <p>另請參閱 <a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> ExportJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ImageServingPublishJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>影像伺服發佈工作的詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>影像演算發佈工作的詳細資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videopublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：VideoPublishJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>視訊發佈工作的詳細資料。 </p> <p>另請參閱 <a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> 視訊發佈工作</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>伺服器目錄發佈工作的詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploaddirectoriejob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：UploadDirectoryJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>上載目錄工作的詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：UploadUrlsJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>上傳URL工作的詳細資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：OptimizeImagesJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：RipPdfJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：重新處理資產工作</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> automatedSetGenerationJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>使用自動化集合指令碼將資產清單處理為集合。 </p> <p>另請參閱 <a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(submitJobReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| jobHandle | `xsd:string` | 是 | 工作控制代碼。 |

## 示例 {#section-40ac77d14adf4588ba2575be6879b2d2}

此程式碼範例會將影像伺服發佈工作提交至IPS並傳回工作控制代碼。 在請求中僅選擇一種工作型別。 因為 `userHandle` 省略，會傳送電子郵件通知給提交工作的使用者。 此範例工作會立即執行，因為 `execTime` 和 `execSchedule` 被省略。

**请求**

```java
<submitJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobName>My Test Job</jobName>
   <imageServingPublishJob>
      <publishType>Full</publishType>
      <emailSetting>Error</emailSetting>
   </imageServingPublishJob>
</submitJobParam>
```

**响应**

```java
<submitJobReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobHandle>47|My Test Job|</jobHandle>
</submitJobReturn>
```

## 说明 {#section-0f3078e503a249aeb6f3d662a51f036a}

您最多可以指定 `execTime` 和 `execSchedule`. 如果兩者皆未傳遞，工作就會立即執行。 您只能使用下列其中一項：

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`
