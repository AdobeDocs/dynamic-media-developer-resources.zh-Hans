---
description: 返回所有公司的数组。
solution: Experience Manager
title: getAllCompanies
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 19%

---


# getAllCompanies{#getallcompanies}

返回所有公司的数组。

语法

## 授权用户类型{#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## 参数 {#section-efd74992e6904ebabe7383b577af4fdb}

**输入(getAllCompaniesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`includeExpired`*` | `xsd:boolean` | 是 | 设置为true可返回过期和未过期的公司。 |

**输出(getAllCompaniesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyArray`*` | `types:CompanyArray` | 是 | 公司数组。 |

## 示例 {#section-3eecf4e6900b41fb92a0e3214791c6b9}

此代码示例返回数组中IPS中的所有公司。 注意，为了简短起见，样本响应被截断。

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

