---
description: 提交新的批处理作业。
solution: Experience Manager
title: batjobsubmit
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 4ab2f6e4-cd68-4f1e-ab54-6f5e9bfc87cb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 2%

---

# batjobsubmit{#batchjobsubmit}

提交新的批处理作业。

此参数：

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 作业数据  </span> </p> </td> 
  <td class="stentry"> <p>完整作业数据的XML代码段。 </p> </td> 
 </tr> 
</table>

返回：

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>作业状态 </p> </td> 
  <td class="stentry"> <p>提交是成功还是失败；如果成功，则作业ID为XML格式。 </p> </td> 
 </tr> 
</table>

## 示例 {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
