---
description: 重新命名資產。
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 7%

---

# renameAsset{#renameasset}

重新命名資產。

>[!NOTE]
>
>此 `renameFiles` 舊版已棄用引數，並已從以下版本中移除： `renameAsset`. 虛擬檔案路徑會變更為符合新的資產名稱（保留副檔名），而實體檔案路徑則不受影響。 API使用者端在更新至新API版本時需要移除此引數的參考。

## 授權的使用者型別 {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資產的讀取和寫入存取權。

## 参数 {#section-ef95a994106841e0ab346dd4cf672258}

**輸入(renameAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 資產所屬公司的控制代碼。 |
| assetHandle | `xsd:string` | 是 | 您要重新命名的資產的控制代碼。 |
| newName | `xsd:string` | 是 | 資產的新名稱。 |
| validateName | `xsd:boolean` | 是 | 如果 `validateName` 是 `true` 且資產型別需要唯一的IPS ID，則會檢查新名稱是否有全域唯一性，以及 `renameAsset` 如果錯誤不是唯一的，則會擲回錯誤。 |

**輸出(renameAssetReturn)**

IPS API未傳回此作業的回應。 請參閱「 」的說明 `<ns1:validateName>` 元素，以取得關於此元素的警告。

## 示例 {#section-a0ddffd62bec42e09069f22ceb486f8a}

此程式碼範例會重新命名資產

**请求**

```java
<ns1:renameAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:newName>My Newly Renamed Image</ns1:newName>
   <ns1:validateName>true</ns1:validateName>
   <ns1:renameFiles>true</ns1:renameFiles>
</ns1:renameAssetParam>
```

**响应**

无。
