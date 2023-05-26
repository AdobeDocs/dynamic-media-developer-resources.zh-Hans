---
description: 使用属性数组更新属性集。
solution: Experience Manager
title: updatePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bbe6a664-b6e1-4b46-867d-a134070b13da
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 15%

---

# updatePropertySet{#updatepropertyset}

使用属性数组更新属性集。

语法

## 授权用户类型 {#section-116693bbfb5d44219e62bbb1ba19de96}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-98361b063e9c41e8b2f744fabc0e13ed}

**输入(updatePropertySetparam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| setHandle | `xsd:string` | 是 | 属性集的句柄。 |
| replaceProperties | `xsd:string` | 否 | 设置为 `true` 以替换属性。 |
| propertyArray | `types:PropertyArray` | 是 | 属性集的已更新属性数组。 |

**输出(updatePropertySetReturn)**

IPS API未返回此操作的响应。

## 示例 {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

此代码示例使用属性数组中的属性更新属性集。

**请求**

```java
<updatePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
   <replaceProperties>true</replaceProperties>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>false</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7teton.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7teton:8080/is/image/</value>
      </items>
   </propertyArray>
</updatePropertySetParam>
```

**响应**

无。
