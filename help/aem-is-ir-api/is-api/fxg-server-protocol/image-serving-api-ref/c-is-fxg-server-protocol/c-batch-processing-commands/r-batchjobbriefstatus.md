---
description: 检索已提交作业的摘要状态。
solution: Experience Manager
title: batchobprif
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 1%

---


# batchjobprifstatus{#batchjobbriefstatus}

检索已提交作业的摘要状态。

此参数：

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>提交时获得的作业ID。 </p> </td> 
 </tr> 
</table>

退货：

XML格式的作业的简要状态；如果jobid无效或作业已删除，则出错。

## 示例 {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
