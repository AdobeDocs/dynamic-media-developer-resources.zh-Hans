---
description: 检索已提交作业的输出。
solution: Experience Manager
title: batjobgetoutput
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 3fb48c39-b15a-45b7-9aca-ed33f9c46c93
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 1%

---

# batjobgetoutput{#batchjobgetoutput}

检索已提交作业的输出。

此参数：

<table id="simpletable_D8AA325968AD4FAEA7B214F0CBBF3F08"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>提交时获取的作业ID。 </p> </td> 
 </tr> 
</table>

返回：

作业的PDF输出作为响应流式处理；如果`jobid`无效或作业已被删除，则出错。

## 示例 {#section-0319e615fa254132a9dab59351b4c252}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobgetoutput&jobid=1005907604914d8eb63126b98f7172n76a5]
