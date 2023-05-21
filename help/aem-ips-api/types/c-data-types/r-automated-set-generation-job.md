---
description: 使用資產控制代碼清單陣列將檔案分組到組中。
solution: Experience Manager
title: AutomatedSetGenerationJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 44df6dfa-1485-40c2-8a14-bbf451b87641
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 7%

---

# [!DNL AutomatedSetGenerationJob]{#automatedsetgenerationjob}

使用資產控制代碼清單陣列將檔案分組到組中。

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
   <td colname="col2"> <span class="codeph"> 型別：HandleArray</span> </td> 
   <td colname="col3">用來建立該集的資產控制代碼陣列。 <p>依預設，1000是您可以在陣列中擁有的最大資產數量。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL destFolder]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 要儲存集合的資料夾路徑。 依預設儲存至公司根資料夾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL readyForPublish]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 設定旗標以指出是否應該發佈資產。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL autoSetCreationOptions]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AutoSetCreationOptions</span> </td> 
   <td colname="col3">您可以在上傳檔案上執行的一組產生命令檔陣列。 另請參閱 <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> 自動設定建立選項</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL emailSetting]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>為工作設定自動化電子郵件通知。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**電子郵件設定選項**

此 `emailSetting` parameter包含以下選項：

| 选项 | 傳回 |
|---|---|
| `All` | 指定收件者的所有工作通知（錯誤、警告、完成）。 |
| `Error` | 指定收件者的工作錯誤。 |
| `ErrorAndWarning` | 給指定收件者的工作錯誤和警告。 |
| `JobCompletion` | 給指定收件者的工作完成通知。 |
| `None` | 工作未將任何工作通知傳送給指定的收件者。 |

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
