---
description: 获取公司作业日志的详细信息。
solution: Experience Manager
title: getJobLogDetails
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d2e4eea6-041b-4a80-beda-cbb8d74cd50b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 11%

---

# getJobLogDetails{#getjoblogdetails}

获取公司作业日志的详细信息。

`logMessage`响应字段已基于`authHeader` `locale`字段进行本地化。

## 授权用户类型 {#section-6f720a7baad64eb3805868c88af9a960}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-47d411a755224c23a4521f10341d66ab}

**输入(getJobLogDetailsParam)**

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
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 作业日志所属公司的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">作业句柄</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 活动作业或已完成作业的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">原始名称</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 作业日志的原始名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 一个或多个日志类型常量。 如果存在，则仅返回指定的日志类型。 默认情况下，返回所有日志类型。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">条记录PerPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：int</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">要返回的<span class="codeph">个detailArray</span>项的最大数目。 最大值和默认值为1000。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">结果页面</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：int</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">要返回的<span class="codeph">个recordsPerPage</span> — 结果的页数。 預設值為 1。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>任务详细信息排序字段常量值（日期或LogType）之一。 默认值为Date。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>Sort Direction字符串常量之一。 默认值为升序。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**输出(getJobLogDetailsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| jobLogArray | `types:JobLogArray` | 是 | 作业日志数组。 |

## 示例 {#section-007678b8b8d94e8f91d09f6bc855f394}

此代码示例返回特定公司的所有作业日志详细信息。 第一个阵列包含标准作业日志详细信息。 嵌入式数组返回有关作业的其他信息。

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
