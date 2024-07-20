---
description: 删除组。
solution: Experience Manager
title: deleteGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0de188de-b4b6-4f48-9918-bcf962fa9482
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 11%

---

# deleteGroup{#deletegroup}

删除组。

语法

## 授权用户类型 {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-42775102ec724c36ae5241eea1a00b8e}

**输入(deleteGroupParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 属于要删除的组的公司的句柄。 |
| groupHandle | `xsd:string` | 是 | 要删除的组的句柄。 |

**输出(deleteGroupParam)**

IPS API不返回此操作的响应。

## 示例 {#section-8f8501af3b3348a1b5701cf9622bf6e4}

此示例代码从公司中删除组。 它需要一个组句柄，您必须从另一个操作获取该句柄。

**请求**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**响应**

无。
