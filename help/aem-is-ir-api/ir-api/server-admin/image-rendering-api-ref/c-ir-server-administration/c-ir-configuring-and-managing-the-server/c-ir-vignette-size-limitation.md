---
description: 「影像演算」會對非金字塔暈映強制執行200萬畫素大小限制。
solution: Experience Manager
title: 暈映大小限制
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# 暈映大小限制{#vignette-size-limitation}

「影像演算」會對非金字塔暈映強制執行200萬畫素大小限制。

修改值 `IrMaxNonPyrVignetteSize` 在[！DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]如果您的應用程式需要支援影像區域（寬度x高度）大於此限制的非金字塔暈映。

>[!NOTE]
>
>`attribute::MaxPix` 和 `IS::MaxMessageSize` 可能也需要調整，以允許異常大的回應影像大小。 如需詳細資訊，請參閱影像伺服檔案。
