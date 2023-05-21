---
description: 工作執行後的工作記錄。
solution: Experience Manager
title: 工作記錄檔
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 3%

---

# [!DNL JobLog]{#joblog}

工作執行後的工作記錄。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| companyHandle | `xsd:string` | 公司控點。 |
| jobHandle | `xsd:string` | 工作控制代碼。 |
| jobName | `xsd:string` | 作业名称. |
| 原始工作名稱 | `xsd:string` | 為工作提交的原始名稱，使用 `submitJob`. |
| submitUserEmail | `xsd:string` | 提交工作之使用者的電子郵件地址。 |
| logType | `xsd:string` | 選擇工作記錄型別。 |
| jobSubType | `xsd:string` | 其他工作資訊。 |
| startDate | `xsd:dateTime` | 工作的開始日期、時間和時區。 |
| endDate | `xsd:dateTime` | 工作的結束日期、時間和時區。 |
| [!DNL description] | `xsd:string` | 工作說明，如原本指定 `submitJob`. |
| fileSuccessCount | `xsd:int` | 已成功處理的檔案數。 |
| fileErrorcount | `xsd:int` | 導致錯誤的檔案數。 |
| fileWarningCount | `xsd:int` | 產生警告的檔案數。 |
| fileDuplicateCount | `xsd:int` | 重複檔案數。 |
| fileUpdateCount | `xsd:int` | 已更新的檔案數。 |
| totalFileCount | `xsd:int` | 記錄的工作處理的檔案數。 |
| transferSuccessCount | `xsd:int` | 成功傳輸的次數。 |
| transferErrorCount | `xsd:int` | 傳輸錯誤數。 |
| transferWarningCount | `xsd:int` | 傳輸警告的數量。 |
| fatalError | `xsd:boolean` | 工作是否產生嚴重錯誤。 |
| detailTotalRows | `xsd:int` | 符合查詢的總列數，可能大於 `detailArray` 因為頁面大小限制。 |
| detailArray | `types:JobLogDetailArray` | 有關記錄工作的詳細資訊陣列。 |
