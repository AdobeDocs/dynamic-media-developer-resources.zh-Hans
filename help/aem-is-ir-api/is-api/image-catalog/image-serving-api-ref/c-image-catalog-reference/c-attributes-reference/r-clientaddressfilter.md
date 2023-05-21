---
description: 使用者端IP位址篩選器。 允許指定一個或多個IP位址或位址範圍。
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

使用者端IP位址篩選器。 允許指定一個或多個IP位址或位址範圍。

指定後，系統會拒絕從未列出的IP位址之使用者端對此影像目錄提出的要求。

## 屬性 {#section-d785265988324af68835410c9ba54147}

以逗號分隔的IP位址清單，含選用的網路遮罩（使用CIDR標籤法）：

`*`ipAddress`*` `[`/ *`netmask`*`]`&#42; `[`，*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p>中的IP位址 <span class="varname"> ddd.ddd.ddd.ddd</span> 格式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 網路遮罩</span> </p></td> 
  <td class="stentry"> <p>網路遮色片（0到32）。 </p></td> 
 </tr> 
</table>

當具有下列專案的前置處理規則時，會忽略此屬性 `<addressfilter>` 元素之後便會套用。

## 默认 {#section-de26e8c9225745e985e4beac1f03f4f6}

繼承自 `default::AddressFilter` 如果未定義或為空。

## 示例 {#section-a955314d2b6a4213a16c12a8b18d8627}

無存取限制： `0.0.0.0/0`

從192開始授與所有位址的存取權： `192.0.0.0/8`

授予512台主機對192.168.12.0到192.168.13.255之間位址的存取權： `192.168.12.0/23`

授予對單一IP位址的存取權： `192.168.2.117` 或 `192.168.2.117/32`

## 另请参阅 {#section-4ea89a7d82e14a4a800487d2d8801465}

[地址篩選器](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
