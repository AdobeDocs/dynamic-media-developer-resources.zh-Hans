---
description: 属性集类型指定用于帮助管理属性集的各种设置。
seo-description: 属性集类型指定用于帮助管理属性集的各种设置。
seo-title: createPropertySetType
solution: Experience Manager
title: createPropertySetType
topic: Dynamic Media Image Production System API
uuid: ecbaad48-d725-4f7a-a37d-5e4cde3295cb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 11%

---


# createPropertySetType{#createpropertysettype}

属性集类型指定用于帮助管理属性集的各种设置。

语法

## 授权用户类型{#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-43dece72eb9f44df80f4a119dd2c008b}

**输入(createPropertySetTypeParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 否 | 拥有属性集类型的公司的句柄。 如果未传递`companyHandle`且调用者为`IpsAdmin`，则将创建全局属性集类型。 |
| `*`name`*` | `xsd:string` | 是 | 属性集类型的名称。 |
| `*`propertyType`*` | `xsd:string` | 是 | 属性集类型的选择。 |
| `*`allowMultiple`*` | `xsd:boolean` | 是 | 确定项目是否可以有多个属性集。 |

**输出(createPropertySetTypeReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | 是 | 类型的手柄。 |

## 示例 {#section-13396c9639a6475190e622eae3cdb534}

此代码示例创建一个属性集，该属性集的名称和类型由`PropertySet Types`常量指定。 拥有属性集类型的公司的句柄。 如果companyHandle未传递，且调用者是IpsAdmin，则将创建全局属性集类型。

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

