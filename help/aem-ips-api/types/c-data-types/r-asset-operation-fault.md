---
title: AssetOperationFault
description: 包含有關批次資產作業期間產生的警告或錯誤條件的資訊。 程式碼和原因欄位會對應到對等的非批次作業所引發的錯誤訊息欄位。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 7%

---

# [!DNL AssetOperationFault]{#assetoperationfault}

包含有關批次資產作業期間產生的警告或錯誤條件的資訊。 程式碼和原因欄位會對應到對等的非批次作業所引發的錯誤訊息欄位。

语法

## 参数 {#section-c906f052f43e4785ba46d92b514b0923}

| 名称 | 类型 | 说明 |
|---|---|---|
| assetHandle | `xsd:string` | 失敗操作的資產控制代碼。 |
| 代码 | `xsd:int` | 作業錯誤碼。 |
| 原因 | `xsd:string` | 錯誤說明或原因。 |
