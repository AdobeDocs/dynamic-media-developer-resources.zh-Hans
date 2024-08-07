---
description: 获取与类型句柄关联的属性集。
solution: Experience Manager
title: getPropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da6923c3-9b86-4595-8205-645fb10e03b0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 16%

---

# getPropertySet{#getpropertysets}

获取与类型句柄关联的属性集。

语法

## 授权用户类型 {#section-da858360b72941bfa8d9558b4da7d4da}

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

**输入(getPropertySetsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| typeHandle | `xsd:string` | 是 | 属性集类型的句柄。 |
| primaryOwnerHandle | `xsd:string` | 是 | 绑定到数据库对象的数据的主要所有者。 |
| secondaryOwnerHandle | `xsd:string` | 否 | 数据的可选辅助所有者。 |

**输出(getPropertySetsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| setArray | `types:PropertySetArray` | 是 | 属性集数组。 |

## 示例 {#section-1358af974eab4259864910337a6f0bd2}

此代码示例返回其主所有者的属性集，这些属性集由类型句柄指定。

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
