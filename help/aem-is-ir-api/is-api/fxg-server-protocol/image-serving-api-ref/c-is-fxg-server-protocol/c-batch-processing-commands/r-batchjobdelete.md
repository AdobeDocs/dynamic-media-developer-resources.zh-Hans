---
description: 删除作业的输出。
solution: Experience Manager
title: batjobdelete
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 1%

---

# batjobdelete{#batchjobdelete}

删除作业的输出。

如果作业当前正在运行，则该作业将立即停止，并删除其所有处理信息。 如果作业成功完成，则会删除其输出文件。

此参数：

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>提交时获取的作业ID。 </p></td> 
 </tr> 
</table>

返回：

在收到删除请求时作业的状态，如果`jobid`无效或作业已被删除，则出现错误。

## 示例 {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
