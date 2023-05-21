---
title: 列印功能
description: 檢視器可讓您將目錄內容輸出到印表機。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# 列印功能{#print-feature}

檢視器可讓您將目錄內容輸出到印表機。

列印功能是由工具列中的專用按鈕所觸發。 按一下按鈕可讓使用者選擇列印範圍及每張紙的頁數。

列印品質可透過以下方式調整： `printquality` 設定引數。 設定 `printquality` 不建議將值設為高於預設值。 原因是因為它會導致使用者端系統上的網頁瀏覽器耗用大量記憶體。 此外，請確定為您的Dynamic Media Classic公司設定的影像回應大小上限大於設定的 `printquality` 值。

>[!NOTE]
>
>Internet Explorer 9以外的桌上型電腦系統才提供「列印」功能。
