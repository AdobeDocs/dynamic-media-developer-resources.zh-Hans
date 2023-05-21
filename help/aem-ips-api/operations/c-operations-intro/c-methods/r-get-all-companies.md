---
description: 傳回所有公司的陣列。
solution: Experience Manager
title: getAllCompanies
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0e339ecf-83b5-410c-8683-f3d73bd92339
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 21%

---

# getAllCompanies{#getallcompanies}

傳回所有公司的陣列。

语法

## 授權的使用者型別 {#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## 参数 {#section-efd74992e6904ebabe7383b577af4fdb}

**輸入(getAllCompaniesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| includeExpired | `xsd:boolean` | 是 | 設為true可傳回過期和未過期的公司。 |

**輸出(getAllCompaniesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyArray | `types:CompanyArray` | 是 | 公司陣列。 |

## 示例 {#section-3eecf4e6900b41fb92a0e3214791c6b9}

此程式碼範例會傳回陣列中IPS中的所有公司。 請注意，為簡短起見，範例回應會遭截斷。

**请求**

```java
<ns1:getAllCompaniesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeExpired>false</ns1:includeExpired>
</ns1:getAllCompaniesParam>
```

**响应**

```java
<ns1:getAllCompaniesReturnxmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyArray>
      <ns1:items>
         <ns1:companyHandle>18</ns1:companyHandle>
         <ns1:name>00webload</ns1:name>
         <ns1:rootPath>00webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.667Z</ns1:expires>
      </ns1:items>
      <ns1:items>
         <ns1:companyHandle>19</ns1:companyHandle>
         <ns1:name>01webload</ns1:name>
         <ns1:rootPath>01webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.414Z</ns1:expires>
      </ns1:items>
      . . .
   </ns1:companyArray>
</ns1:getAllCompaniesReturn>
```
