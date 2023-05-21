---
description: 屬性集是應用程式專用的名稱 — 值組集合，可根據屬性集型別附加到各種IPS物件。 如果屬性集型別不允許將多個集合附加至物件(PropertySetType/allowMultipleisfalse)，而且物件已經有相同型別的關聯集合，則新集合會取代現有集合。
solution: Experience Manager
title: createPropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e9f85e65-4a2f-4b82-b7b8-d0d60b8345cd
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 8%

---

# createPropertySet{#createpropertyset}

屬性集是應用程式專用的名稱 — 值組集合，可根據屬性集型別附加到各種IPS物件。 如果屬性集型別不允許將多個集合附加至物件(PropertySetType/allowMultipleisfalse)，而且物件已經有相同型別的關聯集合，則新集合會取代現有集合。

语法

## 授權的使用者型別 {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-25258e75f5f3419bad165c797eb6cd8e}

**輸入(createPropertySetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| typeHandle | `xsd:string` | 是 | 屬性集型別的控制代碼。 |
| primaryOwnerHandle | `xsd:string` | 是 | 屬性集主要擁有者的控制代碼。 |
| secondaryOwnerHandle | `xsd:string` | 否 | 屬性集的次要擁有者的控制代碼。 |
| propertyArray | `types:PropertyArray` | 是 | 屬性的陣列。 |
| permissionArray | `types:PermissionUpdateArray` |  |  |

**輸出(createPropertySetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| setHandle | `xsd:string` | 是 | 新屬性集的控制代碼。 |

## 示例 {#section-4e1f5b2883664bc88f590fcd253df22b}

此程式碼範例會建立包含屬性名稱和值的屬性集。 回應會傳回新屬性集的控制代碼。

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
