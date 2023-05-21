---
description: 使用這些伺服器設定進行記錄存取。
solution: Experience Manager
title: 存取記錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e677a617-115d-4f6e-9eb5-bdc14ad7ff24
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 4%

---

# 存取記錄{#access-logging}

使用這些伺服器設定進行記錄存取。

语法

## TC：：directory — 記錄檔資料夾 {#section-5d9e2168d4504bbe9868b7d6051c9d67}

資料夾的 [!DNL Platform Server] 寫入記錄檔。 這可以是絕對路徑，也可以是相對於 *`install_folder`*. 預設為 [!DNL  *`install_folder`*/logs].

>[!NOTE]
>
>在變更此設定之前，必須先建立新資料夾。 如果「影像伺服」安裝成以root以外的使用者帳戶執行，請確定資料夾具有正確的讀取/寫入存取許可權。

## TC：：maxDays — 保留記錄檔的天數 {#section-45cbecffc5694c87b7d5c176a44a4885}

記錄檔應保留的天數。 每天的午夜都會建立新的記錄檔。 此時，伺服器將刪除記錄檔資料夾中所有超過指定天數的檔案，包括由影像伺服器或轉譯伺服器寫入的檔案。 默认值为 10。

## TC：：prefix — 存取記錄檔名稱 {#section-1003856323b844049632710a5a056aa7}

寫入存取記錄檔資料的檔案名稱前置詞。 日期和檔案字尾( [!DNL  *`yyyy`*-*`mm`*-*`dd`*.log])附加至指定的字串。 存取記錄檔的名稱必須與追蹤記錄檔的名稱不同。 默认值为 &quot; `access-`&quot;.

## TC：：pattern — 存取記錄模式 {#section-22775ea85cee444d8a7d7336a3b1feef}

指定資料模式 [!DNL Platform Server] 存取記錄檔記錄。 圖樣字串會指定以對應值取代的變數。 模式字串中的所有其他字元會按字面意義傳輸到記錄中。

若要使用快取準備公用程式，必須將空格當作欄位分隔符號使用。 此 [!DNL Platform Server] 將欄位值中的所有空格和&#39;%&#39;字元取代為 `%20` 和 `%25`（分別）。

支援下列模式變數：

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>圖樣</b> </th> 
   <th class="entry"> <b>说明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> %a </span> </p> </td> 
   <td> <p>遠端IP位址。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %A </span> </p> </td> 
   <td> <p>本機IP位址。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %b </span> </p> </td> 
   <td> <p>回應位元組計數不包括HTTP標頭，或如果為零則為' '。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>回應位元組計數，不包括HTTP標頭。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>要求處理時間（毫秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>執行緒id （用於交叉參照偵錯/錯誤記錄專案）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>日期和時間，格式為 <span class="codeph"> <span class="varname"> yyyy </span>- <span class="varname"> 公厘 </span>- <span class="varname"> dd </span> <span class="varname"> HH </span>： <span class="varname"> 公厘 </span>： <span class="varname"> ss </span>. <span class="varname"> SSS </span> offset </span> </p> <p> ( <span class="varname"> SSS </span> 為毫秒， <span class="varname"> offset </span> 是GMT時間位移)；會在將回應傳送至使用者端時擷取時間值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>要求方法( <span class="codeph"> GET </span>， <span class="codeph"> POST </span>，依此類推)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>請求重疊（同時處理的請求數）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>收到此要求的本機連線埠。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>查詢字串（以「？」開頭） （如果存在）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>第一行要求（要求方法、URI、HTTP版本）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p>與 <span class="codeph"> %r </span>，但會對URI套用有限的HTTP編碼，以避免記錄剖析問題。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>HTTP回應狀態代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %S </span> </p> </td> 
   <td> <p>使用者工作階段ID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>日期和時間，使用一般記錄格式。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>已驗證的遠端使用者（如果有的話），否則"。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U </span> </p> </td> 
   <td> <p>uri路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v </span> </p> </td> 
   <td> <p>本機伺服器名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T </span> </p> </td> 
   <td> <p>要求處理時間（以秒為單位）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] 快取金鑰（快取檔案資料夾/名稱）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] 快取管理關鍵字： <span class="codeph"> { REUSED |已建立 |已更新 |遠端 |遠端建立 |遠端更新 | REMOTE_CACHE |已驗證 |已忽略 |未定義} </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r </span> </p> </td> 
   <td> <p>回應MIME型別。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>如果前後關聯發生，則為目的地前後關聯。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r </span> </p> </td> 
   <td> <p>此 <span class="codeph"> etag </span> 回應標頭值（回應資料的MD5簽章）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r </span> </p> </td> 
   <td> <p>错误消息. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r </span> </p> </td> 
   <td> <p>從影像伺服器擷取快取專案或資料所花費的時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r </span> </p> </td> 
   <td> <p>請求剖析和影像目錄查閱所花的時間。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r </span> </p> </td> 
   <td> <p>指出此要求是否嘗試過目錄系統以外的任何路徑型存取。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r </span> </p> </td> 
   <td> <p>快取叢集中傳遞快取專案的對等伺服器的IP位址，或是'-' （如果） <span class="codeph"> 快取使用 </span> 兩者皆非 <span class="codeph"> REMOTE_CREATED </span> 也不 <span class="codeph"> REMOTE_UPDATES </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r </span> </p> </td> 
   <td> <p>錯誤類別： </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=無錯誤。 </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=在伺服器上找不到影像。 </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=IS通訊協定使用錯誤或1以外的內容錯誤。 </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=其他伺服器錯誤。 </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=請求因暫時伺服器超載而遭拒。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r </span> </p> </td> 
   <td> <p>的上限大小寫值 <span class="codeph"> req= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r </span> </p> </td> 
   <td> <p>請求主要目錄的根ID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r </span> </p> </td> 
   <td> <p>所需的時間 [!DNL Platform Server] 以在將資料寫入輸出資料流後傳送回應。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r </span> </p> </td> 
   <td> <p>按讚 <span class="codeph"> %B </span>，但包含304 （未修改）回應的值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformedUrl}r </span> </p> </td> 
   <td> <p>所有規則集轉換後的最終URL。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpRequestHeader </span>}i </span> </p> </td> 
   <td> <p>指定HTTP要求標頭的值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpResponseHeader </span>} </span> </p> </td> 
   <td> <p>指定的HTTP回應標頭的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

默认值为 `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
