---
title: 透過HTTP POST將資產上傳至UploadFile Servlet
description: 將資產上傳至 [!DNL Dynamic Media] Classic涉及一個或多個HTTPPOST請求，這些請求會設定一個工作，以協調與上傳檔案相關的所有記錄活動。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 3%

---

# 透過HTTP POST將資產上傳至UploadFile Servlet{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

將資產上傳到Dynamic Media Classic中涉及一個或多個HTTPPOST請求，這些請求會設定一個工作來協調與上傳檔案關聯的所有記錄活動。

使用下列URL存取UploadFile Servlet：

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>上傳工作的所有POST請求都必須來自相同的IP位址。

**Dynamic Media地區的存取URL**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>地理位置 </p> </th> 
   <th colname="col2" class="entry"> <p>生產URL </p> </th> 
   <th colname="col3" class="entry"> <p>預備URL （用於生產前的開發和測試） </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>北美 </p> </td> 
   <td colname="col2"> <p> https://s7sps1ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps1ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>歐洲、中東、亞洲 </p> </td> 
   <td colname="col2"> <p> https://s7sps3ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps3ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>日本/亞太地區 </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## 上傳工作的工作流程 {#section-873625b9512f477c992f5cdd77267094}

上傳工作包含一或多個使用通用的HTTP POST `jobHandle` 將處理關聯至相同工作。 每個請求都是 `multipart/form-data` 編碼並包含下清單單元件：

>[!NOTE]
>
>上傳工作的所有POST請求都必須來自相同的IP位址。

|  HTTPPOST表單部分  |  说明  |
|---|---|
| `auth`  |   必需. 指定驗證和使用者端資訊的XML authHeader檔案。 另請參閱 **要求驗證** 在 [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
| `file params`  |   可选. 您可以包含一或多個要連同每個POST請求一起上傳的檔案。 每個檔案零件都可在Content-Disposition標頭中包含一個檔案名稱引數，如果沒有，則用作IPS中的目標檔案名稱 `uploadPostParams/fileName` 引數已指定。 |

|  HTTPPOST表單部分   |  uploadPostParams元素名稱   |  类型   |  说明   |
|---|---|---|---|
| `uploadParams` (必需. XML `uploadParams` 指定上傳引數的檔案)   |   `companyHandle`  |  `xsd:string`  | 必需. 檔案要上傳到的公司的控制代碼。  |
| `uploadParams` (必需. XML `uploadParams` 指定上傳引數的檔案) | `jobName`  |  `xsd:string`  | 兩者之一 `jobName` 或 `jobHandle` 為必填欄位。 上載工作的名稱。  |
| `uploadParams` (必需. XML `uploadParams` 指定上傳引數的檔案) | `jobHandle`  |  `xsd:string`  | 兩者之一 `jobName` 或 `jobHandle` 為必填欄位。 處理在上一個請求中啟動的上傳工作。  |
| `uploadParams` (必需. XML `uploadParams` 指定上傳引數的檔案) | `locale`  |  `xsd:string`  | 可选. 本地化的語言和國家/地區代碼。  |
| `uploadParams` (必需. XML `uploadParams` 指定上傳引數的檔案) | `description`  |  `xsd:string`  | 可选. 工作的說明。  |
| `uploadParams` (必需. XML `uploadParams` 指定上傳引數的檔案) | `destFolder`  |  `xsd:string`  | 可选. 檔案名稱屬性前置詞的目標資料夾路徑，特別是針對檔案名稱中可能不支援完整路徑的瀏覽器和其他使用者端。  |
| `uploadParams` (必需. XML `uploadParams` 指定上傳引數的檔案) | `fileName`  |  `xsd:string`  | 可选. 目標檔案的名稱。 覆寫檔案名稱屬性。 |
| `uploadParams` (必需. XML `uploadParams` 指定上傳引數的檔案) | `endJob`  |  `xsd:boolean`  | 可选. 默认值为 false。 |
| `uploadParams` (必需. XML `uploadParams` 指定上傳引數的檔案) | `uploadParams`  |  `types:UploadPostJob`  | 如果這是現有作用中工作的後續請求，則此選項為選用。 如果有現有工作， `uploadParams` 會略過並使用現有的工作上傳引數。 另請參閱 [UploadpostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

在內 `<uploadPostParams>` 區塊是 `<uploadParams>` 指定處理所包含檔案的區塊。

另請參閱 [UploadpostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

雖然您可能會假設 `uploadParams` 但同一作業中的個別檔案引數可能會變更，情況並非如此。 使用相同的 `uploadParams` 整個工作的引數。

新上傳工作的初始POST請求應指定 `jobName` 引數，最好使用唯一的工作名稱，以簡化後續的工作狀態輪詢和工作記錄查詢。 相同上載工作的其他POST請求應指定 `jobHandle` 引數而非 `jobName`，使用 `jobHandle` 從初始請求傳回的值。

上載工作的最終POST請求應將 `endJob` 引數為true，以便此工作日後不會發佈任何檔案。 反過來，這可讓工作在擷取所有POSTed檔案後立即完成。 否則，如果未在30分鐘內收到其他POST請求，則作業會逾時。

## uploadpost回應 {#section-421df5cc04d44e23a464059aad86d64e}

對於成功的POST請求，回應本文是XML `uploadPostReturn` 檔案，如XSD在下列專案中所指定：

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

此 `jobHandle` 傳回的內容傳入 `uploadPostParams`/ `jobHandle` 相同工作的任何後續POST請求的引數。 您也可以使用它來輪詢工作狀態 `getActiveJobs` 作業或透過查詢工作記錄檔 `getJobLogDetails` 作業。

如果處理POST請求時發生錯誤，則回應內文會由其中一種API錯誤型別組成，如所述 [錯誤](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## 範例POST請求 {#section-810fe32abdb9426ba0fea488dffadd1e}

```{.line-numbers}
POST /scene7/UploadFile HTTP/1.1 
User-Agent: Jakarta Commons-HttpClient/3.1 
Host: localhost 
Content-Length: 362630 
Content-Type: multipart/form-data; boundary=O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
  
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="auth" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <authHeader xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03">  
                   <user>sampleuser@test.com</user>  
                   <password>*</password>  
                   <locale>en-US</locale>  
                   <appName>MyUploadServletTest</appName>  
                   <appVersion>1.0</appVersion>  
                   <faultHttpStatusCode>200</faultHttpStatusCode>  
           </authHeader>                   
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="uploadParams" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <uploadPostParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
                <companyHandle>c|2101</companyHandle> 
                <jobName>uploadFileServlet-1376682217351</jobName> 
                <uploadParams> 
                    <overwrite>true</overwrite> 
                    <readyForPublish>true</readyForPublish> 
                    <preservePublishState>true</preservePublishState> 
                    <createMask>true</createMask> 
                    <preserveCrop>true</preserveCrop> 
                    <manualCropOptions> 
                      <left>500</left> 
                      <right>500</right> 
                      <top>500</top> 
                      <bottom>500</bottom> 
                    </manualCropOptions> 
                    <photoshopOptions> 
                      <process>MaintainLayers</process> 
                      <layerOptions> 
                        <layerNaming>AppendNumber</layerNaming> 
                        <anchor>Northwest</anchor> 
                        <createTemplate>true</createTemplate> 
                        <extractText>true</extractText> 
                        <extendLayers>false</extendLayers> 
                      </layerOptions> 
                    </photoshopOptions> 
                    <emailSetting>None</emailSetting> 
                </uploadParams> 
            </uploadPostParam>        
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file1"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-1.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file2"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-2.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ--
```

## 範例POST回應 — 成功 {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## 範例POST回應 — 錯誤 {#section-efc32bb371554982858b8690b05090ec}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
