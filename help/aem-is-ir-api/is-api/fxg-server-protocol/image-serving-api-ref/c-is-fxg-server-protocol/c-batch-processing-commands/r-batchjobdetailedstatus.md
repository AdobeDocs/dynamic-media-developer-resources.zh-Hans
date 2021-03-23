---
description: 检索已提交作业的详细状态。
seo-description: 检索已提交作业的详细状态。
seo-title: batchjobdetailedstatus
solution: Experience Manager
title: batchjobdetailedstatus
uuid: a79302ce-745b-44d8-9cb6-ed8d37530197
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---


# batchjobdetailsedstatus{#batchjobdetailedstatus}

检索已提交作业的详细状态。

此参数：

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>提交时获得的作业ID。 </p> </td> 
 </tr> 
</table>

退货：

XML格式作业的详细状态；如果`jobid`无效或作业已删除，则出错。

## 示例 {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
