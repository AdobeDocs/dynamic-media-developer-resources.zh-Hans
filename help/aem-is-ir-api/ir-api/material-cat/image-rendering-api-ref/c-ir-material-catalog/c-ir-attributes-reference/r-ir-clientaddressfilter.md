---
title: ClientAddressFilter
description: 使用者端IP位址篩選器。 允許指定一個或多個IP位址或位址範圍。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# ClientAddressFilter{#clientaddressfilter}

使用者端IP位址篩選器。 允許指定一個或多個IP位址或位址範圍。

指定後，系統會拒絕從未列出的IP位址之使用者端對此影像目錄提出的要求。 `localhost` 永遠是 `ClientAddressFilter` 定義，即使未明確指定。 請求來自 `localhost` 不會被拒絕，不論 `ClientAddressFilter` 規格。

## 屬性 {#section-21a2992f108d42fb8660c0d65aa61e13}

以逗號分隔的IP位址清單，含選用的網路遮罩([CIDR標籤法](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) 已使用)：

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* 中的IP位址 *[!DNL ddd.ddd.ddd.ddd]* 格式

* *[!DNL netmask]* 網路遮色片（0到32）

當具有下列專案的預處理規則時，會忽略此屬性： `<addressfilter>` 元素之後便會套用。

## 默认 {#section-beddaa18ed6c4f3ba1eb2d4471267712}

繼承自 `default::AddressFilter` 如果未定義或為空。

## 示例 {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* 無存取限制： `0.0.0.0/0`
* 授與所有位址的存取權，開頭為 `192: 192.0.0.0/8`
* 將512部主機的存取權授與位址介於 `192.168.12.0` 和 `192.168.13.255: 192.168.12.0/23`

* 授予對單一IP位址的存取權： `192.168.2.117` 或 `192.168.2.117/32`

## 另请参阅 {#section-6198780c7b3045aabd211eefb38bc565}

[地址篩選器](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
