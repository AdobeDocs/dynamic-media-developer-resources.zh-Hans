---
description: 使用這些伺服器設定來設定監視和警示系統。
solution: Experience Manager
title: 監視和警示系統
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# 監視和警示系統{#monitoring-and-alerting-system}

使用這些伺服器設定來設定監視和警示系統。

## AS：：monitorAlertGenerator.enableGlobalAlerting — 警示系統啟用 {#section-612f8ea61794426ab205e22e5f665fa9}

將設為「true」並設定電子郵件通知設定，以啟用電子郵件通知。 設定為 `false` 關閉所有電子郵件警示 — 這在讓伺服器離線進行維護時很有用。 布尔值.

## AS：：mailSender.host - SMTP主機 {#section-151df07e7b44446581339bb7abeeba7a}

SMTP電子郵件伺服器的IP位址。

## AS：：mailSender.port- SMTP連線埠 {#section-4b25efca8fd84d5c92dafacd0555e99d}

SMTP電子郵件伺服器的接聽連線埠。

## AS：：monitorAlertGenerator.messageTo — 訊息收件者 {#section-0017bbaa15434117a70900c3f1163960}

應傳送警示的一或多個電子郵件地址。 使用分號做為分隔符號。

## AS：：monitorAlertGenerator.messageFrom — 訊息寄件者 {#section-db320cba4ac2438ca1cfe6abce4aed87}

此電子郵件應使用於 **[!UICONTROL 從]** 電子郵件欄位。

## AS：：monitorAlertGenerator.alertInterval — 監督間隔 {#section-99cb2e3380c1499e9d5aec3671ed73c7}

監督系統會在警示間隔期間累積警示條件，並在每個間隔結束時傳送包含所有累積警示的警示電子郵件。 毫秒、整數值60000或更大。 通常設定為5或10分鐘。

## AS：：monitorAlertGenerator.heapSpaceResetInterval — 棧積空間警示間隔 {#section-fd5a2bf04ed44fdcaef20f77084151a8}

棧積空間警示之後發出另一個棧積空間警示之前的最短時間。 間隔時間（毫秒）。 整數值（0或更大）。

## AS：：monitorAlertGenerator.minTrafficForAlerts — 啟用警示的最小流量 {#section-8b4db2d6f96642309ca35c49eb3ab230}

每秒要求數。 如果流量低於此臨界值，則不會發出任何回應時間和錯誤警示。 設為0可傳送回應時間和錯誤警示，無論流量為何。 大於或等於0的實數值。
