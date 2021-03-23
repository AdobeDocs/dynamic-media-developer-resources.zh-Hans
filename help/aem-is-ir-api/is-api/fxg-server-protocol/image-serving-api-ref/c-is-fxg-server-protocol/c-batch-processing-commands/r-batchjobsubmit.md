---
description: 提交新的批作业。
seo-description: 提交新的批作业。
seo-title: batchjobsubmit
solution: Experience Manager
title: batchjobsubmit
uuid: eb695666-fcaf-40bc-8b56-452819f058d2
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 1%

---


# batchjobsubmit{#batchjobsubmit}

提交新的批作业。

此参数：

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobdata  </span> </p> </td> 
  <td class="stentry"> <p>完整作业数据的XML片段。 </p> </td> 
 </tr> 
</table>

退货：

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>作业状态 </p> </td> 
  <td class="stentry"> <p>提交是成功还是失败；如果成功，作业ID采用XML格式。 </p> </td> 
 </tr> 
</table>

## 示例 {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
