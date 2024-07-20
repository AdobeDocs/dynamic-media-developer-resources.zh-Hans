---
description: 使用资源句柄列表数组将文件分组到组中。
solution: Experience Manager
title: AutomatedSetGenerationJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 44df6dfa-1485-40c2-8a14-bbf451b87641
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 4%

---

# [!DNL AutomatedSetGenerationJob]{#automatedsetgenerationjob}

使用资源句柄列表数组将文件分组到组中。

语法

## 参数 {#section-939b2e6946a64238be3709fec2cd0b84}

<table id="table_0E031B2014B646BDA2A94D7E0B55DD5B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL assetHandleArray]</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：HandleArray</span> </td> 
   <td colname="col3">用于创建资源集的资源句柄数组。 <p>默认情况下，1000是您可以在数组中拥有的最大资源数。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL destFolder]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 要保存集合的文件夹的路径。 默认保存到公司根文件夹。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL readyForPublish]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3"> 设置标志以指示是否应发布资产。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL autoSetCreationOptions]</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：AutoSetCreationOptions</span> </td> 
   <td colname="col3">您可以在上传文件上运行的一组生成脚本。 查看<a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL emailSetting]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>为作业设置自动电子邮件通知。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**电子邮件设置选项**

`emailSetting`参数包含以下选项：

| 选项 | 返回 |
|---|---|
| `All` | 向指定收件人发送的所有作业通知（错误、警告、完成）。 |
| `Error` | 指定收件人的作业错误。 |
| `ErrorAndWarning` | 向指定收件人发送作业错误和警告。 |
| `JobCompletion` | 向指定收件人发送作业完成通知。 |
| `None` | 作业不会向指定的收件人发送任何作业通知。 |

## 示例 {#section-d01ee7671f274a1fa12737e8df91d2cf}

```
<complexType name="AutomatedSetGenerationJob">
  <sequence>
    <element name="assetHandleArray" type="types:HandleArray"/>
    <element name="destFolder" type="xsd:string" minOccurs="0"/>
    <element name="readyForPublish" type="xsd:boolean"/>
    <element name="autoSetCreationOptions" type="types:AutoSetCreationOptions"/>
    <element name="emailSetting" type="xsd:string"/>
  </sequence>
</complexType>
```
