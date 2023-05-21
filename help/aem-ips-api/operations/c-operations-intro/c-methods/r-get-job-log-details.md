---
description: 取得公司工作記錄檔的詳細資料。
solution: Experience Manager
title: getJobLogDetails
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d2e4eea6-041b-4a80-beda-cbb8d74cd50b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 18%

---

# getJobLogDetails{#getjoblogdetails}

取得公司工作記錄檔的詳細資料。

此 `logMessage` 回應欄位已根據 `authHeader` `locale` 欄位。

## 授權的使用者型別 {#section-6f720a7baad64eb3805868c88af9a960}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-47d411a755224c23a4521f10341d66ab}

**輸入(getJobLogDetailsParam)**

<table id="table_A77122D73F684B3F8F5AFA1C11C189ED"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 必需 </th> 
   <th colname="col4" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 工作記錄檔所屬公司的控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 作用中或已完成工作的控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 原始名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 工作記錄檔的原始名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 一或多個「記錄型別」常數。 如果存在，則只會傳回指定的記錄型別。 依預設，會傳回所有記錄型別。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">最大數量 <span class="codeph"> detailArray</span> 要傳回的專案。 最大值和預設值為1000。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">頁碼 <span class="codeph"> recordsPerPage</span>-results以傳回。 預設值為 1。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortby</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>工作詳細資料排序欄位常數值之一（日期或LogType）。 預設值為Date。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>排序方向字串常數之一。 預設值為升序。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(getJobLogDetailsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| jobLogArray | `types:JobLogArray` | 是 | 工作記錄陣列。 |

## 示例 {#section-007678b8b8d94e8f91d09f6bc855f394}

此程式碼範例會傳回特定公司的所有工作記錄檔詳細資料。 第一個陣列包含標準作業記錄檔詳細資訊。 內嵌陣列會傳回有關作業的其他資訊。

**请求**

```java
<ns1:getJobLogDetailsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:jobHandle>47||Add_2007-09-14-15:04:34</ns1:jobHandle>
</ns1:getJobLogDetailsParam>
```

**响应**

```java
<getJobLogDetailsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>some_address@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
         <detailArray>
            <items>
               <logMessage>Upload has begun!</logMessage>
               <logType>BeginUpload</logType>
            </items>
            <items>
               <logMessage>Add_2007-09-14-15:04:34</logMessage>
               <logType>OriginalJobName</logType>
            </items>
            <items>
               <logMessage>s7oslo</logMessage>
               <logType>JobClient</logType>
            </items>
            ...
         </detailArray>
      </items>
   </jobLogArray>
</getJobLogDetailsReturn>
```
