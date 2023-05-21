---
description: 設定各種公司專屬的設定值。
solution: Experience Manager
title: setcompanysettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 12%

---

# setcompanysettings{#setcompanysettings}

設定各種公司專屬的設定值。

语法

## 授權的使用者型別 {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-a472da6c57c74a94a179dda081004888}

**輸入(setCompanySettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司控點。 |
| overwriteMode | `xsd:string` | 否 | 資產覆寫模式。 |
| retainPublishState | `xsd:boolean` | 否 | 設定為 `true` 重新上傳資產時保留發佈狀態。 |
| defaultSourceProfileHandle | `xsd:string` | 否 | IccProfile資產，以做為預設來源色彩設定檔。 |
| defaultDisplayProfileHandle | `xsd:string` | 否 | IccProfile資產，以做為預設的顯示色彩設定檔。 |
| iptcExifMappingXsltHandle | `xsd:string` | 否 | 用於將IPTC和EXIF中繼資料對應到IPS中繼資料欄位的XSL資產。 |
| Xmappingxslthandle | `xsd:string` | 否 | 用於將XMP中繼資料對應至IPS中繼資料欄位的XSL資產。 |
| diskSpaceWarningMin | `xsd:int` | 否 | 傳送警告訊息之前可用的最小可用磁碟空間(KB)。 |
| emailTrashCleanupWarning | `xsd:boolean` | 否 | 設定為 `true` 若要在資產從垃圾桶清空時傳送通知給公司管理員。 |

**輸出(setCompanySettingsReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

此程式碼範例會設定公司的設定。

**请求**

```java
<ns1:setCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
   <ns1:overwriteMode>OverwriteFullName</ns1:overwriteMode>
   <ns1:retainPublishState>true</ns1:retainPublishState>
   <ns1:diskSpaceWarningMin>100000</ns1:diskSpaceWarningMin>
   <ns1:emailTrashCleanupWarning>true</ns1:emailTrashCleanupWarning>
</ns1:setCompanySettingsParam>
```

**响应**

无。
