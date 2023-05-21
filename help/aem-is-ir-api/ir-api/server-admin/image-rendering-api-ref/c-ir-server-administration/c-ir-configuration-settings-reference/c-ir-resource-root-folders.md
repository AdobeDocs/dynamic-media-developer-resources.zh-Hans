---
description: 路徑清單（以分號分隔）可作為具有相對檔案路徑的所有資料檔案的根。
solution: Experience Manager
title: 資源根資料夾(ir.resourceRootPaths)
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# 資源根資料夾(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

路徑清單（以分號分隔）可作為具有相對檔案路徑的所有資料檔案的根。

可以是絕對路徑，也可以是相對於 *[!DNL install_folder]*. 指定多個路徑時，伺服器會嘗試以指定順序建立每個根目錄，直到找到檔案為止。 預設為 [!DNL ./resources]，代表預設根路徑 [!DNL install_folder/resources].
