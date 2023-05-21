---
description: 刪除群組。
solution: Experience Manager
title: deleteGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0de188de-b4b6-4f48-9918-bcf962fa9482
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 13%

---

# deleteGroup{#deletegroup}

刪除群組。

语法

## 授權的使用者型別 {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-42775102ec724c36ae5241eea1a00b8e}

**輸入(deleteGroupParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 屬於您要刪除之群組的公司控制代碼。 |
| groupHandle | `xsd:string` | 是 | 您要刪除之群組的控制代碼。 |

**輸出(deleteGroupParam)**

IPS API未傳回此作業的回應。

## 示例 {#section-8f8501af3b3348a1b5701cf9622bf6e4}

此範常式式碼會從公司中刪除群組。 它需要群組控制代碼，您必須從其他作業取得此控制代碼。

**请求**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**响应**

无。
