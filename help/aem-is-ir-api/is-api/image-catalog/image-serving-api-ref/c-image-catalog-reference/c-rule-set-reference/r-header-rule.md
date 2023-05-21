---
description: HTTP回應標頭元素。 選填於 <rule> 元素。
solution: Experience Manager
title: header
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 4%

---

# header{#header}

HTTP回應標頭元素。 選填於 `<rule>` 元素。

## 属性 {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*文字*&quot;** ：必填。 指定HTTP標頭的名稱。

**`Action`= &quot;set&quot; |`"add"`**：選擇性。 預設為 `"set"`，會取代任何目前的標頭值。 指定 `"add"` 以附加標頭值，並以逗號分隔。

## 数据 {#section-a387f541396c49d99c29692a38032914}

標頭值。

## 说明 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

允許新增新的HTTP回應標頭，以及新增或取代預先定義標頭的值。 名稱和值必須符合HTTP標準。 不會套用其他編碼。

「影像伺服」替代變數可用於標頭名稱和標頭值。 這可讓您從請求中控制兩個字串。

## 示例 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

當請求中的標頭值指定為變數時，下列規則會套用自訂標頭：

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

此規則由以下要求觸發，設定HTTP回應標頭 `Edge-Control::no-store`：

`http://server/is/image/cat/id?$Edge-Control=no-store`
