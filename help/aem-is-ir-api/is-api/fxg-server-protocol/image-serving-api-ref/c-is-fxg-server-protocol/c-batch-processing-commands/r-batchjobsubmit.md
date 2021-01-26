---
description: 提交新的批作业。
seo-description: 提交新的批作业。
seo-title: batchjobsubmit
solution: Experience Manager
title: batchjobsubmit
topic: Dynamic Media Image Serving - Image Rendering API
uuid: eb695666-fcaf-40bc-8b56-452819f058d2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 2%

---


# batchjobsubmit{#batchjobsubmit}

提交新的批作业。

此参数：

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 作业数据  </span> </p> </td> 
  <td class="stentry"> <p>完整作业数据的XML片段。 </p> </td> 
 </tr> 
</table>

退货：

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>作业状态 </p> </td> 
  <td class="stentry"> <p>提交是否成功；如果成功，作业ID采用XML格式。 </p> </td> 
 </tr> 
</table>

## 示例 {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
