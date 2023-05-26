---
description: 管理按组访问、修改、创建或删除资产的权限。
solution: Experience Manager
title: 权限
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 13%

---

# [!DNL Permission]{#permission}

管理按组访问、修改、创建或删除资产的权限。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| groupHandle | `xsd:string` | 组句柄。 |
| groupName | `xsd:string` | 群组名称. |
| permissionType | `xsd:string` | 权限类型的选择。 |
| isAllowed | `xsd:boolean` | 确定是否允许该权限。 |
| isOverride | `xsd:boolean` | 确定权限是否覆盖其他权限。 |
