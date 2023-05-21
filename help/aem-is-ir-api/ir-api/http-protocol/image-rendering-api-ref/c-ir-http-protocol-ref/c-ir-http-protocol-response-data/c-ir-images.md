---
title: 图像
description: 如果要求成功完成，且要求不包含req=命令，或req=有下列其中一個值img， debug，則會傳回影像資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---

# 图像{#images}

如果要求成功完成，且要求未包含req=命令，或req=有下列其中一個值，則會傳回影像資料： img、debug

HTTP回應MIME型別由以下專案決定 `fmt=`，或，如果 `fmt=` 未指定，它取決於 `attribute::Format`.

如果要求方法為無條件，則HTTP回應狀態為「200 OK」 `GET` 或 `HEAD`.

伺服器可能會以「304」狀態回覆（未修改），並且不會傳回任何影像資料來回應條件 `GET` 請求(使用 [!DNL If-Modified-Since] 存在於中的欄位 `request-header`)。
