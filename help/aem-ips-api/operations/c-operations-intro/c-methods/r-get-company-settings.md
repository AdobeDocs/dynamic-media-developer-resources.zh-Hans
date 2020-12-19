---
description: 返回特定公司的IPS设置。
seo-description: 返回特定公司的IPS设置。
seo-title: getCompanySettings
solution: Experience Manager
title: getCompanySettings
topic: Scene7 Image Production System API
uuid: 28ee706d-aaef-45a1-9655-3805f158cdc3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 22%

---


# getCompanySettings{#getcompanysettings}

返回特定公司的IPS设置。

语法

## 授权用户类型{#section-3378c9c67029473a87d5f5d8c616b1f3}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-e146f479c2744baa8f68be8c8848c97f}

**输入(getCompanySettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 要检索其设置的公司的句柄。 |

**输出(getCompanySettingsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`设置`*` | `types:CompanySettings` | 是 | 公司设置。 |

## 示例 {#section-191f78995ecf473a95eadf7296204fd7}

此代码示例返回特定公司的所有IPS设置。

**请求**

```java
<ns1:getCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
</ns1:getCompanySettingsParam>
```

**响应**

```java
<getCompanySettingsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <settings>
      <metadataArray>
         <items>
            <name>Profile Class</name>
            <value>1</value>
            <longVal>1</longVal>
         </items>
         <items>
             <name>Default Color Profile</name>
             <value>1</value>
         </items>
      </metadataArray>
      <iccProfileInfo>
         <originalPath>Scene7SharedAssets/ICCColorProfiles/Adobe ICC Profiles/RGB Profiles/</originalPath>
         <originalFile>sRGB Color Space Profile.icm</originalFile>
         <fileSize>0</fileSize>
      </iccProfileInfo>
      </defaultDisplayProfile>
      <diskSpaceWarningMin>100000</diskSpaceWarningMin>
      <emailTrashCleanupWarning>true</emailTrashCleanupWarning>
   </settings>
</getCompanySettingsReturn>
```

