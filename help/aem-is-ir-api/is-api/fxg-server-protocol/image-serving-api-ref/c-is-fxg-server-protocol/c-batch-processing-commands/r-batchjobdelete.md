---
description: 删除作业的输出。
seo-description: 删除作业的输出。
seo-title: batchjobdelete
solution: Experience Manager
title: batchjobdelete
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d19ed1c8-e13b-4da4-90e3-6bb0dcce2a12
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 1%

---


# batchjobdelete{#batchjobdelete}

删除作业的输出。

如果作业当前正在运行，则会立即停止该作业，并删除其所有处理信息。 如果作业成功完成，则其输出文件将被删除。

此参数：

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>提交时获得的工作ID。 </p></td> 
 </tr> 
</table>

退货：

收到删除请求时的作业状态，如果`jobid`无效或作业已被删除，则出错。

## 示例 {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
