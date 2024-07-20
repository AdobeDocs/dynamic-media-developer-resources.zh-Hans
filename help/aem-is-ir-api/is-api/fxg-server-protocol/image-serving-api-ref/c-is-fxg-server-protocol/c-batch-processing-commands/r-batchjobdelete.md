---
title: batchjobdelete
description: 删除作业的输出。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# batchjobdelete{#batchjobdelete}

删除作业的输出。

如果某个作业当前正在运行，则会立即停止该作业，并删除其所有处理信息。 如果作业已成功完成，则会删除其输出文件。

此参数：

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> job_id</span> </p> </td> 
  <td class="stentry"> <p>提交时获取的作业ID。 </p></td> 
 </tr> 
</table>

返回：

收到删除请求时的作业状态，如果`jobid`无效或作业已被删除则出现错误。

## 示例 {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5`
