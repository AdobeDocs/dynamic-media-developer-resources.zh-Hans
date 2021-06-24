---
description: 属性集类型指定用于帮助管理属性集的各种设置。
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 11%

---

# createPropertySetType{#createpropertysettype}

属性集类型指定用于帮助管理属性集的各种设置。

语法

## 授权用户类型 {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-43dece72eb9f44df80f4a119dd2c008b}

**输入(createPropertySetTypeParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 否 | 拥有资产集类型的公司的句柄。 如果未传递`companyHandle`并且调用方为`IpsAdmin`，则将创建全局属性集类型。 |
| `*`name`*` | `xsd:string` | 是 | 属性集类型的名称。 |
| `*`propertyType`*` | `xsd:string` | 是 | 属性集类型的选择。 |
| `*`allowMultiple`*` | `xsd:boolean` | 是 | 确定您的程序是否可以具有多个资产集。 |

**输出(createPropertySetTypeReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | 是 | 类型的句柄。 |

## 示例 {#section-13396c9639a6475190e622eae3cdb534}

此代码示例创建一个属性集，该属性集的名称和类型由`PropertySet Types`常量指定。 拥有资产集类型的公司的句柄。 如果未传递companyHandle，且调用方是IpsAdmin，则将创建全局属性集类型。

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
