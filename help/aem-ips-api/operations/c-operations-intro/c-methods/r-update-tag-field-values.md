---
description: 更新标记字段的标记词典值。
seo-description: 更新标记字段的标记词典值。
seo-title: updateTagFieldValues
solution: Experience Manager
title: updateTagFieldValues
uuid: 21689469-a0dd-480b-82ba-ebd12956ff8f
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 14%

---


# updateTagFieldValues{#updatetagfieldvalues}

更新标记字段的标记词典值。

语法

## 授权用户类型{#section-0372b742b1344979b0668faacb36fcc6}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-0a3a4bab026746238c9d4009caf42e94}

**Input(updateTagFieldValuesParam)**

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
   <td colname="col4"> 公司手柄。 </td> 
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
   <td colname="col4">要更新的标记字段值的数组。 <p>注意： 仅更新标记字符串值。 不会影响资产关联。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**输出(updateTagFieldValuesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功更新的标记字段数。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作尝试更新标记字段时生成的警告数。 |
| `*`errorCount`*` | `xsd:int` | 是 | 操作尝试更新标记字段时生成的错误数。 |
| `*`warningDetailArray`*` | `types:TagValueUpdateFaultArray` | 否 | 在操作尝试更新标记字段时生成警告的与资产关联的详细信息数组。 |
| `*`errorDetailArray`*` | `types:TagValueUpdateFaultArray` | 否 | 在操作尝试更新标记字段时生成错误的与资产关联的详细信息数组。 |

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

