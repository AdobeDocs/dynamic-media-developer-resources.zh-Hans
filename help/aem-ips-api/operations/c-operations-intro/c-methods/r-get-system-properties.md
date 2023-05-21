---
description: 擷取單一請求中的所有系統屬性。
solution: Experience Manager
title: getSystemProperties
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b0ef16fd-1645-4e22-99bb-8c9269623168
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 20%

---

# getSystemProperties{#getsystemproperties}

擷取單一請求中的所有系統屬性。

语法

## 授權的使用者型別 {#section-fc311ce90a54400fa95b9dd36b756e23}

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

**輸入(getSystemPropertiesParam)**

无。

**輸出(getSystemPropertiesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| propertyArray | `types:PropertyArray` | 是 | 系統屬性的陣列。 |

## 示例 {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

此程式碼範例會傳回系統屬性的陣列。 回應因簡短而遭截斷。

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
