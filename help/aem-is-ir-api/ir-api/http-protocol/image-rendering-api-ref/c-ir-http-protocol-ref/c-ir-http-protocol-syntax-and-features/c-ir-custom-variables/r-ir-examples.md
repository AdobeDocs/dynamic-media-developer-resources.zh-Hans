---
title: 示例
description: 此範例使用「影像伺服」為物件上色，並將包含自訂文字的貼花套用在一組暈映的其中一個中。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 1%

---

# 示例{#examples}

此範例使用「影像伺服」為物件上色，並將包含自訂文字的貼花套用在一組暈映的其中一個中。

IR變數可用來識別暈映、標誌影像和自訂文字。

此 `vignette::Modifier` 記錄中命名的欄位 *範本* 在材質目錄的暈映對映中 `myCat` 包含下列專案：

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

所有使用的暈映都會列在材質目錄的暈映對映中 `myCat`.

使用者端現在可以提出以下要求來擷取預設影像（使用在範本開頭定義的變數）：

[!DNL `https://server/myCat/template`]

以下請求指定要呈現的特定內容：

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

如需影像伺服的詳細資訊，請參閱影像伺服檔案 `text=` 命令。
