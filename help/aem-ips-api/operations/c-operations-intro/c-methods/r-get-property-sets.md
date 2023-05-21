---
description: 取得與型別控制代碼關聯的屬性集。
solution: Experience Manager
title: getPropertySets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da6923c3-9b86-4595-8205-645fb10e03b0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 18%

---

# getPropertySets{#getpropertysets}

取得與型別控制代碼關聯的屬性集。

语法

## 授權的使用者型別 {#section-da858360b72941bfa8d9558b4da7d4da}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-d8da2847e77e4a95a4441d9848cac775}

**輸入(getPropertySetsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| typeHandle | `xsd:string` | 是 | 屬性集型別的控制代碼。 |
| primaryOwnerHandle | `xsd:string` | 是 | 繫結至資料庫物件之資料的主要擁有者。 |
| secondaryOwnerHandle | `xsd:string` | 否 | 資料的可選次要擁有者。 |

**輸出(getPropertySetsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| setArray | `types:PropertySetArray` | 是 | 屬性集陣列。 |

## 示例 {#section-1358af974eab4259864910337a6f0bd2}

此程式碼範例會傳回其主要擁有者的屬性集（由型別控制代碼指定）。

**请求**

```java
<getPropertySetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
</getPropertySetsParam>
```

**响应**

```java
<getPropertySetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setArray>
      <items>
         <setHandle>ps|941</setHandle>
         <typeHandle>pt|10801</typeHandle>
         <propertyArray>
            <items>
               <name>application_server_prefix_published_test</name>
               <value>http://s7teton.macromedia.com:8080/is/image/</value>
            </items>
            <items>
               <name>application_project_whatever</name>
               <value>false</value>
            </items>
            <items>
               <name>application_server_prefix_origin_test</name>
               <value>http://s7teton:8080/is/image</value>
            </items>
         </propertyArray>
      </items>
   </setArray>
</getPropertySetsReturn>
```
