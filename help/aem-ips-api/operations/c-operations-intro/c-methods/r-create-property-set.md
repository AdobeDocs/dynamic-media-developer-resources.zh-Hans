---
description: 属性集是特定于应用程序的名称值对集，可根据属性集类型附加到各种IPS对象。 如果属性集类型不允许将多个集附加到对象(PropertySetType/allowMultipleisfalse)，并且对象已经具有同一类型的关联集，则新集将替换现有集。
solution: Experience Manager
title: createPropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e9f85e65-4a2f-4b82-b7b8-d0d60b8345cd
TQID: 'https://experienceleague.adobe.com/kMRKY0OQPDLsPpPDtTQpxwTBiBu3dco37mSxR7khfgg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 217
ht-degree: 7%

---

# createPropertySet{#createpropertyset}

属性集是特定于应用程序的名称值对集，可根据属性集类型附加到各种IPS对象。 如果属性集类型不允许将多个集附加到对象(PropertySetType/allowMultipleisfalse)，并且对象已经具有同一类型的关联集，则新集将替换现有集。

语法

## 授权用户类型 {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-25258e75f5f3419bad165c797eb6cd8e}

**输入(createPropertySetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| typeHandle | `xsd:string` | 是 | 属性集类型的句柄。 |
| primaryOwnerHandle | `xsd:string` | 是 | 属性集的主要所有者的句柄。 |
| secondaryOwnerHandle | `xsd:string` | 否 | 属性集的辅助所有者的句柄。 |
| propertyArray | `types:PropertyArray` | 是 | 属性数组。 |
| permissionArray | `types:PermissionUpdateArray` |  |  |

**输出(createPropertySetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| setHandle | `xsd:string` | 是 | 新属性集的句柄。 |

## 示例 {#section-4e1f5b2883664bc88f590fcd253df22b}

此代码示例创建一个属性集，其中包含属性的名称和值。 响应将返回新属性集的句柄。

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

