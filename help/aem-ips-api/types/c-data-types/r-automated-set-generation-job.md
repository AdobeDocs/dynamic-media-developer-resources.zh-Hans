---
description: 使用资产句柄列表数组将文件分组为一组。
solution: Experience Manager
title: AutomatedSetGenerationJob
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 44df6dfa-1485-40c2-8a14-bbf451b87641
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 7%

---

# AutomatedSetGenerationJob{#automatedsetgenerationjob}

使用资产句柄列表数组将文件分组为一组。

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
   <td colname="col2"> <span class="codeph"> 类型：HandleArray</span> </td> 
   <td colname="col3">用于创建集的资产句柄数组。 <p>默认情况下，数组中可包含的资产数上限为1000。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 要保存集的文件夹的路径。 默认情况下，保存到公司根文件夹。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 设置一个标志以指示是否应发布资产。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：AutoSetCreationOptions</span> </td> 
   <td colname="col3">可以在上传文件上运行的一组生成脚本数组。 请参阅<a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>为作业设置自动电子邮件通知。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**emailSetting选项**

`emailSetting`参数包括以下选项：

| 选项 | 返回结果 |
|---|---|
| `All` | 指定收件人的所有作业通知（错误、警告、完成）。 |
| `Error` | 指定收件人的作业错误。 |
| `ErrorAndWarning` | 指定收件人的作业错误和警告。 |
| `JobCompletion` | 向指定的收件人发出作业完成通知。 |
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
