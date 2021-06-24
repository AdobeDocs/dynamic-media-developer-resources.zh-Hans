---
description: 更新标记字段的标记字典值。
solution: Experience Manager
title: updateTagFieldValues
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 6de49217-2d15-49d9-9357-b058b2564686
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 15%

---

# updateTagFieldValues{#updatetagfieldvalues}

更新标记字段的标记字典值。

语法

## 授权用户类型 {#section-0372b742b1344979b0668faacb36fcc6}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-0a3a4bab026746238c9d4009caf42e94}

**输入(updateTagFieldValuesParam)**

<table id="table_15F354FBC043464080BC975AE35E03A4"> 
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
   <td colname="col4"> 公司负责人。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 标记字段句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:TagValueUpdateArray</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4">要更新的标记字段值数组。 <p>注意： 仅更新标记字符串值。 不影响资产关联。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output(updateTagFieldValuesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功更新的标记字段数。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作尝试更新标记字段时生成的警告数。 |
| `*`errorCount`*` | `xsd:int` | 是 | 操作尝试更新标记字段时生成的错误数。 |
| `*`warningDetailArray`*` | `types:TagValueUpdateFaultArray` | 否 | 与资产关联的详细信息数组，当操作尝试更新标记字段时，资产会生成警告。 |
| `*`errorDetailArray`*` | `types:TagValueUpdateFaultArray` | 否 | 与在操作尝试更新标记字段时生成错误的资产关联的详细信息数组。 |

## 示例 {#section-bb4dcf97044c4675974c9b8d27674001}

**请求**

```java
<updateTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <updateArray>
      <items>
         <oldValue>Nurth</oldValue>
         <newValue>North</newValue>
      </items>
      <items>
         <oldValue>Suth</oldValue>
         <newValue>South</newValue>
      </items>
      <items>
         <oldValue>East</oldValue>
         <newValue>West</newValue>
      </items>
      <items>
         <oldValue>Banana</oldValue>
         <newValue>Pear</newValue>
      </items>
   </updateArray>
</updateTagFieldValuesParam>
```

**响应**

```java
<updateTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>2</errorCount>
   <errorDetailArray>
      <items>
         <value>East</value>
         <code>30001</code>
         <reason>New tag value 'West' already exists.</reason>
      </items>
      <items>
         <value>Banana</value>
         <code>30001</code>
         <reason>Tag value 'Banana' not found.</reason>
      </items>
   </errorDetailArray>
</updateTagFieldValuesReturn>
```
