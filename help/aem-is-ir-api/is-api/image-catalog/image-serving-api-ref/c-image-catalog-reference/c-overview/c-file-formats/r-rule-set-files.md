---
description: 规则集文件是XML格式的文本文件，必须遵循相应的标准和惯例。
solution: Experience Manager
title: 规则集文件
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f3d700f-1941-4220-b91d-54e78fae6aaf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# 规则集文件{#rule-set-files}

规则集文件是XML格式的文本文件，必须遵循相应的标准和惯例。

[!DNL RuleSet.xsd] 安装在默认目录文件夹中，并且应该用于在将规则集文件提交到图像服务之前对其进行验证。 应用严格解析，并且规则集文件不符合 [!DNL RuleSet.xsd] 不要加载。
