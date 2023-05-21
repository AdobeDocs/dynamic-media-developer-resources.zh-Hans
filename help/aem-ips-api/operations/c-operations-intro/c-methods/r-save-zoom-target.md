---
description: 建立或編輯縮放目標。
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 595fd5c8-4e98-4c1a-b396-c8e170aaf454
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 20%

---

# saveZoomTarget{#savezoomtarget}

建立或編輯縮放目標。

语法

## 授權的使用者型別 {#section-823cd9f0557045bca51da66768b5ba74}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-4a23983cae4e49a098e9bbe736933996}

**輸入(saveZoomTargetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 具有您要儲存之縮放目標的公司的控制代碼。 |
| assetHandle | `xsd:string` | 是 | 縮放目標的控制代碼。 |
| zoomTargetHandle | `xsd:string` | 否 | 編輯或建立縮放目標。 |
| 名称 | `xsd:string` | 是 | 縮放目標名稱。 |
| xPosition | `xsd:int` | 是 | 左側畫素位置。 |
| y位置 | `xsd:int` | 是 | 上方的畫素位置。 |
| 宽度 | `xsd:int` | 是 | 縮放目標寬度。 |
| 高度 | `xsd:int` | 是 | 縮放目標高度。 |
| userData | `xsd:string` | 是 | 客戶特定資訊。 可包含任何型別的資料。 |

**輸出(saveZoomTargetReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| zoomTargetHandle | `xsd:string` | 是 | 處理新建立的縮放目標。 |

## 示例 {#section-509c472c316549cdb228d7e1cfa8400a}

此程式碼範例會儲存縮放目標。 回應會傳回縮放目標控制代碼。

**请求**

```java
<saveZoomTargetParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <name>My Zoom Target</name>
   <xPosition>2</xPosition>
   <yPosition>2</yPosition>
   <width>10</width>
   <height>10</height>
   <userData>My User Data</userData>
</saveZoomTargetParam>
```

**响应**

```java
<saveZoomTargetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <zoomTargetHandle>34194|9|301</zoomTargetHandle>
</saveZoomTargetReturn>
```
