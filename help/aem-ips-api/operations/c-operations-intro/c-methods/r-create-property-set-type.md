---
description: 屬性集型別會指定用來協助管理屬性集的各種設定。
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 12%

---

# createPropertySetType{#createpropertysettype}

屬性集型別會指定用來協助管理屬性集的各種設定。

语法

## 授權的使用者型別 {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-43dece72eb9f44df80f4a119dd2c008b}

**輸入(createPropertySetTypeParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 否 | 擁有屬性集型別的公司的控制代碼。 若 `companyHandle` 未傳遞，且呼叫者為 `IpsAdmin`，則會建立全域屬性集型別。 |
| 名称 | `xsd:string` | 是 | 屬性集型別的名稱。 |
| propertyType | `xsd:string` | 是 | 屬性集型別的選擇。 |
| allowMultiple | `xsd:boolean` | 是 | 決定您的程式是否可以擁有多個屬性集。 |

**輸出(createPropertySetTypeReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| typeHandle | `xsd:string` | 是 | 型別的控制代碼。 |

## 示例 {#section-13396c9639a6475190e622eae3cdb534}

此程式碼範例會建立屬性集，其名稱和型別由 `PropertySet Types` 常數。 擁有屬性集型別的公司的控制代碼。 如果未傳遞companyHandle且呼叫者為IpsAdmin，則會建立全域屬性集型別。

**请求**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10803</typeHandle>
</createPropertySetTypeReturn>
```

**响应**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</createPropertySetTypeReturn>
```
