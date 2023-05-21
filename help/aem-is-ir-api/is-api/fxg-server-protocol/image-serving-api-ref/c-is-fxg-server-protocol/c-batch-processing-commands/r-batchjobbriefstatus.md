---
title: batchjobbriefstatus
description: 擷取已提交工作的摘要狀態。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b31bdbb-3c2c-4f7f-ba95-d3e710270be0
source-git-commit: 13991f71ab54d1003a79a496b861d53a61899bdc
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 2%

---

# batchjobbriefstatus{#batchjobbriefstatus}

擷取已提交工作的摘要狀態。

此引數：

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid </span> </p> </td> 
  <td class="stentry"> <p>提交時取得的作業ID。 </p> </td> 
 </tr> 
</table>

傳回：

XML格式工作的簡短狀態；如果工作ID無效或工作已刪除，則會發生錯誤。

## 示例 {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
