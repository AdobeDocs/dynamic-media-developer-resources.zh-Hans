---
description: 說明IPS Web服務API處理的一般操作引數。
solution: Experience Manager
title: 操作方法
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---

# 操作方法{#operations-methods}

本節說明IPS Web服務API處理的一般作業引數。

如需每個作業引數的完整說明，請參閱 [操作引數](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## 控制代碼：關於 {#section-094ce1afa6244fa5b2c762f44ffdca1c}

處理特定API作業傳回的參考IPS物件。 您也可以將控制代碼作為引數傳遞給後續的操作呼叫。 控制代碼為字串資料型別( `xsd:string`)。

控制代碼僅供在單一應用程式工作階段中使用。 此外，您應該讓控點持續存在，因為其格式可能會在IPS版本之間變更。 當您編寫互動式應用程式時，您會實作工作階段逾時，並捨棄工作階段之間的所有控制代碼，尤其是在IPS升級之後。 當您撰寫非互動式應用程式時，請呼叫適當的作業，以在每次執行應用程式時擷取控制代碼。 下列Java/Axis2程式碼範例顯示不正確且正確的程式碼執行：

**不正確的處理代碼**

此程式碼範例不正確，因為它包含公司控制碼的硬式編碼值(555)。

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**正確的控制代碼**

此程式碼範例正確，因為它會呼叫 `getCompanyInfo` 以傳回有效的控制代碼。 它不仰賴硬式編碼值。 使用此方法（或其他IPS API對等方法）傳回所需的控制代碼。

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## 一般控制代碼型別 {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

大部分作業都要求您透過傳入來設定公司內容 `companyHandle` 引數。 公司控制代碼是某些作業傳回的指標，例如 `getCompanyInfo`， `addCompany`、和 `getCompanyMembership`.

**userHandle**

此 `userHandle` parameter是選擇性引數，適用於以特定使用者為目標的作業。 依預設，這些操作會鎖定呼叫的使用者（其認證已傳入以進行驗證的使用者）。 不過，具有適當許可權的管理員使用者可以指定其他使用者。 例如， `setPassword` 操作通常會設定已驗證使用者的密碼，但管理員可以使用 `userHandle` 引數來設定不同使用者的密碼。

針對需要公司內容的作業(使用 `companyHandle` 引數)，則驗證使用者與目標使用者都必須是指定公司的成員。 對於不需要公司內容的作業，已驗證的使用者和目標使用者都必須是至少一個通用公司的成員。

下列操作可以擷取使用者控制代碼：

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle和accessGroupHandle**

根據預設，需要存取許可權（讀取、寫入、刪除）的操作會在呼叫使用者的許可權內容中操作。 某些作業可讓您修改此前後關聯，使用 `accessUserHandle` 或 `accessGroupHandle` 引數。 此 `accessUserHandle` 引數可讓管理員模擬其他使用者。 此 `accessGroupHandle` 引數可讓呼叫者在特定使用者群組的前後關聯中操作。

**responseFieldArray和excludeFieldArray**

某些作業可讓呼叫者限制回應中包含哪些欄位。 限制欄位有助於減少處理請求所需的時間和記憶體，並降低回應資料的大小。 呼叫者可以透過傳遞來要求特定的欄位清單 `responseFieldArray` 引數，或透過列舉排除的欄位清單 `excludeFieldArray` 引數。

兩者 `responseFieldArray` 和 `excludeFieldArray` 使用節點路徑指定欄位，路徑分隔為 `/`. 例如，若要指定 `searchAssets` 只傳回每個資產的名稱、上次修改日期和中繼資料參考以下內容：

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

同樣地，若要傳回所有欄位（許可權除外）：

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

請注意，節點路徑是相對於傳回節點根目錄的。 如果您指定複雜的型別欄位，但不包含其任何子元素(例如， `assetArray/items/imageInfo`)，則會包含其所有子元素。 如果您在複雜型別欄位中指定一或多個子元素(例如， `assetArray/items/imageInfo/originalPath`)，則只會包含這些子元素。

如果您不包含 `responseFieldArray` 或 `excludeFieldArray` 在請求中，會傳回所有欄位。

**地區設定**

自IPS 4.0起，IPS API支援透過傳遞 `authHeader` locale引數。 如果區域設定引數不存在，則HTTP標頭 `Accept-Language` 已使用。 如果此標頭也不存在，則會使用IPS伺服器的預設地區設定。

某些作業也會使用明確地區設定引數，這些引數可能與作業地區設定內容不同。 例如， `submitJob` 作業需要 `locale` 設定用於作業記錄和電子郵件通知的地區設定的引數。

地區設定引數使用格式 `<language_code>[-<country_code>]`

其中語言代碼是由ISO-639所指定的小寫雙字母代碼，而選用國家/地區代碼是由ISO-3266所指定的大寫雙字母代碼。 例如，美式英文的地區設定字串是 `en-US`.
