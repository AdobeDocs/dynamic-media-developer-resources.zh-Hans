---
description: 「Scene 7影像伺服」包含下列元件
solution: Experience Manager
title: 影像伺服元件
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---

# 影像伺服元件{#image-serving-components}

「Scene 7影像伺服」包含下列元件：

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>元件 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>伺服器監督員 </p> </td> 
   <td colname="col2"> <p>負責啟動、停止及確保其他元件健康狀態的獨立可執行檔。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>為大部分的Java型元件提供環境。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>監視/警示服務 </p> </td> 
   <td colname="col2"> <p>J2EE應用程式。 提供伺服器監控和電子郵件警示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>J2EE應用程式。 管理使用者端連線、記錄、與其他元件的通訊。 HTTP存取於 <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>快取服務 </p> </td> 
   <td colname="col2"> <p>J2EE應用程式。 管理 [!DNL Platform Server]的資料快取。 /is/cache上的HTTP存取。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>图像服务器 </p> </td> 
   <td colname="col2"> <p>執行所有的影像處理和影像檔案I/O作業。 32位元和64位元可執行檔都適用於Linux （32位元僅適用於Windows）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE文字轉譯元件 </p> </td> 
   <td colname="col2"> <p>文字演算服務的一或多個執行個體可能在使用中，當 <span class="codeph"> textPs=</span> 作業執行。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG演算元件 </p> </td> 
   <td colname="col2"> <p>獨立式Java應用程式（非由Tomcat託管）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media影像演算(亦稱為 渲染服务器) </p> </td> 
   <td colname="col2"> <p>需要單獨的授權才能啟用。 HTTP存取於 <span class="filepath"> /ir/render</span>. 所有影像演算功能已整合至 [!DNL Platform Server] 和Image Server ，且沒有個別的可執行元件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

預設目錄( [!DNL default.ini])或特定影像目錄(請參閱 [影像目錄](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) 以取得詳細資訊)。
