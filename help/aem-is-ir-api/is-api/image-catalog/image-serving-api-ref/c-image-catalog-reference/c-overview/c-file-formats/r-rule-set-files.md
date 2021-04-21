---
description: 规则集文件是XML格式的文本文件，必须符合相应的标准和惯例。
solution: Experience Manager
title: 规则集文件
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# 规则集文件{#rule-set-files}

规则集文件是XML格式的文本文件，必须符合相应的标准和惯例。

[!DNL RuleSet.xsd] is installed in default catalog folder， should be used to validate rule set files befor committing the Image Serving.应用严格分析，不符合[!DNL RuleSet.xsd]的规则集文件不加载。