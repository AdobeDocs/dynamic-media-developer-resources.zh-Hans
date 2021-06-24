---
description: 在单个请求中检索所有系统属性。
solution: Experience Manager
title: getSystemProperties
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: b0ef16fd-1645-4e22-99bb-8c9269623168
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 18%

---

# getSystemProperties{#getsystemproperties}

在单个请求中检索所有系统属性。

语法

## 授权用户类型 {#section-fc311ce90a54400fa95b9dd36b756e23}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## 参数 {#section-b2a4fb7068424223aec87c50f0586d73}

**输入(getSystemPropertiesParam)**

无。

**输出(getSystemPropertiesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`propertyArray`*` | `types:PropertyArray` | 是 | 系统属性的数组。 |

## 示例 {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

此代码示例返回一个系统属性数组。 响应因简短而被截断。

**请求**

```java
<getSystemPropertiesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"/>
```

**响应**

```java
<getSystemPropertiesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"> 
   <propertyArray> 
      <items> 
         <name>SvgRenderEnabled</name> 
         <value>true</value> 
      </items> 
      <items> 
         <name>SwfRootUrl</name> 
         <value>/SWFs/</value> 
      </items> 
      ... 
   </propertyArray> 
</getSystemPropertiesReturn>
```
