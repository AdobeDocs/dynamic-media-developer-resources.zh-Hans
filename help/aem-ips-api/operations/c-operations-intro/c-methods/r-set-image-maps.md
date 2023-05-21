---
description: 設定資產的影像地圖。
solution: Experience Manager
title: setImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 11%

---

# setImageMap{#setimagemaps}

設定資產的影像地圖。

您必須已建立影像地圖。 影像地圖會依從陣列擷取的順序套用。 這表示第二個影像地圖會覆蓋第一個，第三個影像地圖會覆蓋第二個影像地圖，依此類推。

## 授權的使用者型別 {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-2292ec1aead947ef8741dd0653a41f42}

**輸入(setImageMapsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司控點。 |
| assetHandle | `xsd:string` | 是 | 資產控點。 |
| imageMapArray | `types:ImageMapDefinitionArray` | 是 | 預先定義的影像地圖陣列。 |

**輸出(setImageMapsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| imageMapHandleArray | `types:HandleArray` | 是 | 將影像地圖控點套用至資產的陣列。 |

## 示例 {#section-fe2e35662a6a4ee29cf250c9fd180371}

此程式碼範例為影像資產設定2個影像地圖。 程式碼會指定叫用影像地圖時採取的形狀型別、區域和動作。 回應包含陣列，其中包含影像對應的控制點。

**请求**

```java
<setImageMapsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <imageMapArray>
      <items>
         <name>ImageMap2</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>true</enabled>
      </items>
      <items>
         <name>ImageMap3</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>false</enabled>
      </items>
   </imageMapArray>
</setImageMapsParam>
```
