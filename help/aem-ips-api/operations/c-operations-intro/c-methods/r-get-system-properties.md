---
description: 检索单个请求中的所有系统属性。
seo-description: 检索单个请求中的所有系统属性。
seo-title: getSystemProperties
solution: Experience Manager
title: getSystemProperties
topic: Scene7 Image Production System API
uuid: 08ea86ba-bde5-45a1-920a-04f784395e6a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getSystemProperties{#getsystemproperties}

检索单个请求中的所有系统属性。

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
| ` *`propertyArray`*` | `types:PropertyArray` | 是 | 系统属性的数组。 |

## 示例 {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

此代码示例返回一组系统属性。 响应因简短而截断。

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

