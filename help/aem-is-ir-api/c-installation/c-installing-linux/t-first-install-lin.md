---
title: 首次安裝
description: 此程式說明如何在Linux®上首次安裝「影像伺服」。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# 首次安裝{#installing-for-the-first-time}

此程式說明如何在Linux®上首次安裝「影像伺服」。

1. 以root許可權登入您的伺服器主機。
1. 建立資料夾 [!DNL /usr/local/scene7/licenses].

   如果影像提供和/或影像演算授權金鑰檔案(包含 [!DNL .sc8] 檔案字尾)，請將其複製到此資料夾。 否則，請繼續安裝，並在稍後安裝授權金鑰。
1. 解壓縮並解壓縮「影像伺服」發佈tar檔案。
1. 在 [!DNL Setup] 資料夾，執行以啟動安裝精靈 [!DNL ./install-is].

   如果找不到授權金鑰，則會顯示說明如何取得授權檔案的指示。 此時請執行此動作，或繼續安裝影像伺服，稍後再安裝授權金鑰。
1. 顯示「一般使用者授權合約(EULA)」時，請閱讀授權合約，然後輸入 `y` 以繼續進行。

   安裝程式會顯示下表列出的提示。

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 主要接聽連線埠[8080]：</span> </p> </td>
   <td colname="col2"> <p>影像提供與影像轉譯的主要HTTP聆聽連線埠。 </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 管理員接聽連線埠[8083]：</span> </p> </td> 
   <td colname="col2"> <p>管理員接聽連線埠。 </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> HTTP快取大小上限(MB) [2000]：</span> </p> </td> 
   <td colname="col2"> <p>主要回應快取的初始大小。 </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 快取根資料夾[/usr/local/scene7/ImageServing/cache]：</span> </p> </td> 
   <td colname="col2"> <p>PS快取資料夾。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 影像伺服器擁有者ID [root]：</span> </p> </td>
   <td colname="col2"> <p>要安裝影像伺服伺服器的使用者帳戶。 </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 影像伺服器群組ID [root]：</span> </p> </td>
   <td colname="col2"> <p>要安裝「影像伺服」伺服器的群組帳戶。 </p> </td>
  </tr>
 </tbody>
</table>

1. 按下 **[!UICONTROL 輸入]** 以接受預設值或指定其他值。

   請確定所有指定的連線埠號碼都是唯一的，而且不會在此主機上使用。

   >[!IMPORTANT]
   >
   >如果指定了root以外的帳戶，您必須確保在組態檔中重新設定這些資料夾時，影像伺服器需要讀取和寫入的所有檔案和資料夾的存取許可權都已正確設定。
   >
   >「影像伺服」現已安裝至 [!DNL /usr/local/Scene7/ImageServing]. 某些影像演算內容已安裝到 [!DNL /usr/local/Scene7/ImageRendering].
   >
   >安裝快要結束時，安裝精靈會嘗試啟動Image Server。 如果找不到有效的授權金鑰，則無法啟動影像伺服器。 如果有有效的授權且Image Server尚未啟動，請查閱記錄檔。

>[!NOTE]
>
>如果在安裝「影像伺服」後安裝了授權，則必須手動啟動影像伺服器才能使用。
