---
description: 检索已提交作业的汇总状态。
seo-description: 检索已提交作业的汇总状态。
seo-title: batchobprip状态
solution: Experience Manager
title: batchobprip状态
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 601e8395-8a77-4324-9cd7-5fe321bc91e3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 1%

---


# batchjobprifstatus{#batchjobbriefstatus}

检索已提交作业的汇总状态。

此参数：

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>提交时获得的工作ID。 </p> </td> 
 </tr> 
</table>

退货：

XML格式作业的简要状态；如果jobid无效或作业已被删除，则出错。

## 示例 {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
