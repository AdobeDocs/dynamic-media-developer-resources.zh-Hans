---
description: 属性集是特定于应用程序的名称——值对集，可以附加到各种IPS对象，具体取决于属性集类型。 如果属性集类型不允许将多个集附加到对象(PropertySetType/allowMultipleisfalse)，并且该对象已具有相同类型的关联集，则新集将替换现有集。
seo-description: 属性集是特定于应用程序的名称——值对集，可以附加到各种IPS对象，具体取决于属性集类型。 如果属性集类型不允许将多个集附加到对象(PropertySetType/allowMultipleisfalse)，并且该对象已具有相同类型的关联集，则新集将替换现有集。
seo-title: createPropertySet
solution: Experience Manager
title: createPropertySet
topic: Dynamic Media Image Production System API
uuid: f0b5b951-143f-4a31-bb6b-cdeabdebbcbb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 6%

---


# createPropertySet{#createpropertyset}

属性集是特定于应用程序的名称——值对集，可以附加到各种IPS对象，具体取决于属性集类型。 如果属性集类型不允许将多个集附加到对象(PropertySetType/allowMultipleisfalse)，并且该对象已具有相同类型的关联集，则新集将替换现有集。

语法

## 授权用户类型{#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-25258e75f5f3419bad165c797eb6cd8e}

**输入(createPropertySetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | 是 | 属性集类型的句柄。 |
| `*`primaryOwnerHandle`*` | `xsd:string` | 是 | 属性集的主要所有者的句柄。 |
| `*`secondaryOwnerHandle`*` | `xsd:string` | 否 | 属性集的辅助所有者的句柄。 |
| `*`propertyArray`*` | `types:PropertyArray` | 是 | 属性的数组。 |
| `*`permissionArray`*` | `types:PermissionUpdateArray` |  |  |

**输出(createPropertySetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | 是 | 新属性集的句柄。 |

## 示例 {#section-4e1f5b2883664bc88f590fcd253df22b}

此代码示例创建一个属性集，其中包含属性的名称和值。 该响应将返回新属性集的句柄。

**请求**

```java
<createPropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>true</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7everest.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7everest:8080/is/image/</value>
      </items>
   </propertyArray>
</createPropertySetParam>
```

**响应**

```java
<createPropertySetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</createPropertySetReturn>
```

