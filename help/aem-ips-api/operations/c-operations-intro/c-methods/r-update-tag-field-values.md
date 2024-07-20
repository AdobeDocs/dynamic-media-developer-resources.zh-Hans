---
description: 更新标记字段的标记字典值。
solution: Experience Manager
title: updateTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6de49217-2d15-49d9-9357-b058b2564686
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 12%

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
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 公司句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 标记字段句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：TagValueUpdateArray</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4">要更新的标记字段值的数组。 <p>注意：仅更新标记字符串值。 不会影响资源关联。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**输出(updateTagFieldValuesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 成功更新的标记字段数。 |
| warningcount | `xsd:int` | 是 | 操作尝试更新标记字段时生成的警告数。 |
| errorCount | `xsd:int` | 是 | 操作尝试更新标记字段时生成的错误数。 |
| warningDetailArray | `types:TagValueUpdateFaultArray` | 否 | 与资源关联的详细信息数组，这些资源在操作尝试更新标记字段时生成警告。 |
| errorDetailArray | `types:TagValueUpdateFaultArray` | 否 | 与资产关联的详细信息数组，在操作尝试更新标记字段时这些资产会生成错误。 |

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

```java {.line-numbers}
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
