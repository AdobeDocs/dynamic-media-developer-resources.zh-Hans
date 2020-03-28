---
description: 检索已提交作业的摘要状态。
seo-description: 检索已提交作业的摘要状态。
seo-title: batchobpriefstatus
solution: Experience Manager
title: batchobpriefstatus
topic: Scene7 Image Serving - Image Rendering API
uuid: 601e8395-8a77-4324-9cd7-5fe321bc91e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchobpriefstatus{#batchjobbriefstatus}

检索已提交作业的摘要状态。

此参数：

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid </span> </p> </td> 
  <td class="stentry"> <p>提交时获得的作业ID。 </p> </td> 
 </tr> 
</table>

退货：

XML格式的作业简况；作业ID无效或作业已删除时出错。

## 示例 {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
