---
description: 刪除工作的輸出。
solution: Experience Manager
title: batchjobdelete
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# batchjobdelete{#batchjobdelete}

刪除工作的輸出。

如果工作目前正在執行，則會立即停止，並刪除其所有處理資訊。 如果工作已成功完成，則會刪除其輸出檔案。

此引數：

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>提交時取得的作業ID。 </p></td> 
 </tr> 
</table>

傳回：

收到刪除請求時的作業狀態，如果出現以下錯誤則出現錯誤 `jobid` 無效或已刪除工作。

## 示例 {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
