---
title: 首次安裝
description: 使用這些步驟在Windows上首次安裝影像伺服。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# 首次安裝{#installing-for-the-first-time}

使用這些步驟在Windows上首次安裝影像伺服。

1. 以管理許可權登入您的伺服器主機。
1. 如果您已經收到授權，請將它複製到您的伺服器，然後按兩下檔案來執行授權安裝。

   如果您還沒有授權，您可以繼續進行安裝，稍後再安裝授權。

1. 解壓縮「影像伺服」發佈zip檔案的內容。
1. 執行以啟動安裝精靈 [!DNL setup]/ [!DNL setup.exe].
1. 選取 **[!UICONTROL 下一個]** 若要前進到使用者授權合約(EULA)，請閱讀授權合約，然後選取 **[!UICONTROL 是]**.

   此 [!DNL Authentication] 對話方塊隨即顯示。
1. 如果已安裝授權，且授權資訊會顯示在 [!DNL Authentication] 對話方塊，選取 **[!UICONTROL 下一個]** 以繼續。

   如果您沒有授權，請選取 **[!UICONTROL 要求授權]**. 下一個對話方塊會顯示您電腦的其中一個網路介面卡MAC位址。 依照提示的指示，透過電子郵件傳送此MAC地址、您的公司名稱以及您正在安裝的產品。

   **重要：** 此授權是以此主機上所安裝的其中一個網路介面卡的MAC位址為基礎。 如果您停用、移除或取代此卡，授權就不再被識別為有效。 請務必取得您用於影像伺服的硬體組態授權。

   您可以在沒有有效授權的情況下繼續安裝IS，稍後再安裝授權。 若要繼續，請選取 **[!UICONTROL 返回]** 以返回 [!DNL Authentication] 對話方塊，然後選取 **[!UICONTROL 下一個]**.
1. 繼續前往&quot;[!DNL Platform Server] 管理員設定」頁面。 視需要輸入新值或接受預設值。

   您可以設定下列專案：

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> [!DNL Platform Server] HTTP連線埠 </p> </td>
      <td> <p>影像提供與影像轉譯的主要HTTP聆聽連線埠 </p> </td>
   </tr> 
   <tr> 
      <td> <p> 管理員接聽連線埠 </p> </td>
      <td> <p>管理員接聽連線埠 </p> </td>
   </tr> 
   <tr> 
      <td> <p> [!DNL Platform Server] 快取大小(MB) </p> </td>
      <td> <p>主要回應快取的初始大小 </p> </td>
   </tr>
   <tr> 
      <td> <p> [!DNL Platform Server] 快取位置 </p> </td>
      <td> <p>PS快取資料夾 </p> </td>
   </tr>
   </tbody>
   </table>

   指定的連線埠號碼必須是唯一的，且不能由其他應用程式或服務使用。

   下一個畫面會提供檢閱所選設定的機會。

1. 選取 **[!UICONTROL 返回]** 進行變更，或選取 **[!UICONTROL 下一個]** 以開始安裝。

1. 選取 **[!UICONTROL 完成]** 以結束安裝精靈。
