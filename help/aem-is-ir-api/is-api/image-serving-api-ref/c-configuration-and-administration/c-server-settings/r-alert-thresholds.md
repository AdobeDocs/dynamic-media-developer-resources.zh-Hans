---
description: 使用這些伺服器設定值來設定警示臨界值。
solution: Experience Manager
title: 警示臨界值
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# 警示臨界值{#alert-thresholds}

使用這些伺服器設定值來設定警示臨界值。

## AS：： monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS：： monitorAlertGenerator.maxAverageResponseTime -Response Time {#section-35111039ac6c4a63ba23fc2c828ab726}

當取樣間隔期間處理要求的平均時間超過此處設定的臨界值時，會發出回應時間警報。 以毫秒為單位表示；整數0或更大。 一般值介於100和1000毫秒之間，視操作的複雜度而定。

>[!NOTE]
>
>此警報不會考慮導致4xx或5xx回應狀態的請求。

## AS：：monitorAlertGenerator.maxErrorRate — 錯誤回應率ThresholdAS：：monitorAlertGenerator.maxErrorRate — 錯誤回應率 {#section-76ba77fd3102419395e0f86719a1f3ec}

當取樣間隔期間的HTTP錯誤回應與總回應之比超過指定的臨界值時，會發出錯誤警報。

介於0.0和1.0之間的實際值。通常設定為0.005和0.1之間。設為1可停用錯誤警示。

## AS：：monitorAlertGenerator.minRequestRate — 低流量臨界值 {#section-8dfb89ed138640fd86f5ce1dae2a533e}

當目前取樣間隔內每秒接收的平均要求數低於此臨界值時，會傳送最小流量警報。 將此值設定為0，停用警示。 以每秒的請求數表示。 大於或等於0的實數值。

## AS：：monitorAlertGenerator.minFreeHeapSpace -Free棧積空間臨界值 {#section-ce6705045f6842769030ccb1894594cc}

指定最小可用Java棧積空間。 當可用棧積空間低於此臨界值時，會在Java垃圾收集循環後立即傳送優先順序警報。 建議使用50 MB以確保 [!DNL Platform Server]. 將可用棧積空間維持在此值以上，可以減少垃圾收集週期的頻率，進而改善整體伺服器效能。 以位元組為單位的整數值，0或更大。

## AS：：monitorAlertGenerator.maxOverlap — 最大並行請求數 {#section-ddc6925bff944758ab19bcc9cf3f2589}

當平均間隔期間同時處理的平均要求數超過此臨界值時，就會觸發重疊警報。 高度重疊可能表示伺服器可能超載的情況。

整數值1或更大。 一般範圍為20到50，視快取命中率和請求複雜度而定。

## AS：：monitorAlertGenerator.lockedThreshold — 鎖定的要求臨界值 {#section-012a1c9937d445708380339279c62d80}

指定要求必須擱置的秒數，超過秒數才會被視為鎖定或擱置。 如果在平均間隔結束時，至少有一個請求處於擱置狀態的時間超過指定的時段，則會發出鎖定的請求警示。 正整數值（以毫秒為單位）。

若要解決涉及從外部HTTP伺服器取得資料的複雜轉譯請求和請求，建議將此值設定為至少30秒（除非此警報會偵測到這類條件）。
