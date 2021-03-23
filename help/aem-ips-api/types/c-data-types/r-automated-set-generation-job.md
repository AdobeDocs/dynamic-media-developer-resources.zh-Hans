---
description: 使用资产句柄列表数组将文件分组到集中。
seo-description: 使用资产句柄列表数组将文件分组到集中。
seo-title: AutomatedSetGenerationJob
solution: Experience Manager
title: AutomatedSetGenerationJob
uuid: 9c664bde-a731-4d6b-ae6b-c862bda02d4c
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 6%

---


# AutomatedSetGenerationJob{#automatedsetgenerationjob}

使用资产句柄列表数组将文件分组到集中。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3">用于创建集的一组资源句柄。 <p>默认情况下，1000是您在数组中可拥有的最大资源数。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 要保存集的文件夹的路径。 默认情况下，保存到公司根文件夹。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 设置一个标志，以指示是否应发布资产。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutoSetCreationOptions</span> </td> 
   <td colname="col3">可以在已上载文件上运行的一组集生成脚本。 请参阅<a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>为作业设置自动电子邮件通知。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**emailSetting选项**

`emailSetting`参数包含以下选项：

| 选项 | 退货 |
|---|---|
| `All` | 指定收件人的所有作业通知（错误、警告、完成）。 |
| `Error` | 指定收件人的作业错误。 |
| `ErrorAndWarning` | 指定收件人的作业错误和警告。 |
| `JobCompletion` | 指定收件人的作业完成通知。 |
| `None` | 作业不会向指定收件人发送任何作业通知。 |

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

