---
title: 自訂變數
description: 請求和暈映修飾元字串的查詢部分可能包含使用者定義的變數。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# 自訂變數{#custom-variables}

請求和暈映：：修飾元字串的查詢部分可能包含使用者定義的變數。

`$ [!DNL name] = [!DNL value]`

`[!DNL name]`  — 變數名稱。 可由字母、數字和安全字元的任意組合組成，但不包括 `$`.

`[!DNL value]`  — 變數要設定的值（字串）。

變數的定義與其他伺服器命令類似，使用上述語法。 必須先定義變數，才能加以參照。 在中定義的變數 `vignette::Modifier` 可在URL要求中參照，反之亦然。

>[!NOTE]
>
>`[!DNL value]` 必須為單通道URL編碼，才能安全HTTP傳輸。 在以下情況下需要雙重編碼 `[!DNL value]` 會透過HTTP重新傳輸。 以下情況即屬於此情況： `[!DNL value]` 會取代為巢狀外部請求。

藉由內嵌變數名稱來參考變數（以開頭與結尾括住） `$`)在命令值中的任意位置。 例如，在 `=`  在命令名稱后面加上後續的 `&` 或要求結尾。 伺服器會取代每個出現的 `$ [!DNL name]$` 替換為 `[!DNL string]`. 在任何情況下都不會發生替代 `$ [!DNL name]$` 在命令名稱（在命令的等號之前）中，以及在請求的路徑部分中。

自訂變數不可巢狀。 任何出現次數 `$ [!DNL name]$` 範圍 `[!DNL string]` 不會被取代。 例如，請求片段 `$var2=apple&$var1=my$var2$tree&text=$var1$` 解析為 `text=my$var2$tree`.

`$` 不是保留字元；可能發生在請求中的其他位置。 例如， `src=my$texture$file.tif` 是有效的指令(假設材料目錄專案或紋理檔案名為 `[!DNL my$texture$file.tif]` 存在)，而 `wid=$number$` 不是，因為 `wid=` 需要數值引數。
