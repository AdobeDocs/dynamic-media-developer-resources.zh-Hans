---
description: 为上传作业自动设置生成脚本列表。 假定为上传指定的每个脚本都会应用于所有上传的资产。
solution: Experience Manager
title: AutoSetCreationOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e6e969be-0410-4be7-88d6-491d715fd137
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 7%

---

# AutoSetCreationOptions{#autosetcreationoptions}

为上传作业自动设置生成脚本列表。 假定为上传指定的每个脚本都会应用于所有上传的资产。

语法

## 参数 {#section-0302e9238dbc4704914e938f42c881e6}

| 名称 | 类型 | 说明 |
|---|---|---|
| autoSetsArray | `types:HandleArray` | 数组 [!DNL PropertySet] 处理定义在上传期间应用的自动设置生成脚本。 |
