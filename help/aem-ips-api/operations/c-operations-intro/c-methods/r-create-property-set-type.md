---
description: 属性集类型指定用于帮助管理属性集的各种设置。
seo-description: 属性集类型指定用于帮助管理属性集的各种设置。
seo-title: createPropertySetType
solution: Experience Manager
title: createPropertySetType
topic: Scene7 Image Production System API
uuid: ecbaad48-d725-4f7a-a37d-5e4cde3295cb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | 否 | 拥有属性集类型的公司的句柄。 如果 `companyHandle` 未传递调用者为调用者 `IpsAdmin`，则将创建全局属性集类型。 |
| ` *`名称`*` | `xsd:string` | 是 | 属性集类型的名称。 |
| ` *`propertyType`*` | `xsd:string` | 是 | 选择属性集类型。 |
| ` *`allowMultiple`*` | `xsd:boolean` | 是 | 确定项目是否可以有多个属性集。 |

**输出(createPropertySetTypeReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`typeHandle`*` | `xsd:string` | 是 | 类型的手柄。 |

## 示例 {#section-13396c9639a6475190e622eae3cdb534}

此代码示例创建一个属性集，其名称和类型由常数指 `PropertySet Types` 定。 拥有属性集类型的公司的句柄。 如果未传递companyHandle且调用者是IpsAdmin，则将创建全局属性集类型。

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

