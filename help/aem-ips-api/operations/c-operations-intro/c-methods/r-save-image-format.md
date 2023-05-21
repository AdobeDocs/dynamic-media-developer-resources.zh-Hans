---
description: 建立影像格式。
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: cafbd715-237b-4454-920e-643f0c84e208
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 12%

---

# saveImageFormat{#saveimageformat}

建立影像格式。

>[!NOTE]
>
>此 `urlModifier` 欄位值必須包含有效的XML。 例如，變更 `&` 至 `&`. 取得 `urlModfier` IPS使用者介面的值。

## 授權的使用者型別 {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**輸入(saveImageFormatParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 具有您要使用之影像格式的公司控制代碼。 |
| imageFormatHandle | `xsd:string` | 否 | 您要儲存的影像格式控制代碼。 |
| 名称 | `xsd:string` | 是 | 影像格式名稱。 |
| urlModifier | `xsd:string` | 是 | 這可以是任何IPS通訊協定查詢字串。 產生URL修飾元的最簡單方式是使用IPS使用者介面建立一個URL，然後剪下並貼上查詢字串。 |

**輸出(saveImageFormatReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| imageFormatHandle | `xsd:string` | 是 | 影像格式的控制代碼。 |

## 示例 {#section-c7bd733212ef494297a97093f3af193f}

此程式碼範例會建立影像格式。 在此範例中， `urlModifier` 是由具有有效HTML格式的IPS使用者介面中的值所決定。

**请求**

```java
<saveImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <name>My Image Format Name</name> 
   <urlModifier>wid=400&amp;hei=400&amp;fmt=jpeg&amp;qlt=750&amp;op_sharpen=0&amp; 
   resMode=bicub&amp;op_usm=0.0,0.0,0,0&amp;iccEmbed=0 
   </urlModifier> 
</saveImageFormatParam>
```

**响应**

```java
<saveImageFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageFormatHandle>47|301</imageFormatHandle> 
</saveImageFormatReturn>
```
