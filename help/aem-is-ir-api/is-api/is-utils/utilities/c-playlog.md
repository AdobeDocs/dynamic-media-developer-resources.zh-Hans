---
description: playlog公用程式可用來預先產生HTTP回應快取的內容。
solution: Experience Manager
title: '''playlog''公用程式'
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0213978-3a1d-44b4-82bf-4527b980b29e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 1%

---

# &#39;playlog&#39;公用程式{#the-playlog-utility}

playlog公用程式可用來預先產生HTTP回應快取的內容。

在進行主要版本升級（當版本號碼的第一位數或第二位數變更時）後，無法保證可使用現有的影像伺服HTTP回應快取。 如果升級後伺服器要即時處於滿載狀態，則伺服器可能會因為快取遺漏請求的前幾個小時而超載，直到合理填入快取且快取命中率增加為止。

若要避免此初始負載尖峰，請 `playlog` 公用程式可用來預先產生HTTP回應快取的內容。 `playlog` 會從現有的存取記錄檔中擷取HTTP要求，並將其傳送至伺服器以產生快取專案。 對於典型的使用案例，播放包含一整天流量的單一存取記錄檔就足夠了。

除了在升級安裝後啟動HTTP回應快取之外，該公用程式還用於在將新伺服器新增到負載平衡環境時預先產生快取內容；只需從其他伺服器之一播放最近的記錄檔即可。

`playlog` 可設定為支援舊版「影像伺服」產生的大多數存取記錄檔。

## 使用 {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p <span class="varname"> 前置詞 </span> </span> </p> </td> 
  <td class="stentry"> <p>根URL會附加在從記錄檔擷取的請求之前。 </p> <p>預設： <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n <span class="varname"> 欄 </span> </span> </p> </td> 
  <td class="stentry"> <p>記錄檔記錄中包含請求的欄位（欄）編號；以1為基礎。 </p> <p>預設： 16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s <span class="varname"> 分隔符號 </span> </span> </p> </td> 
  <td class="stentry"> <p>欄位分隔符號；規則運算式模式。 </p> <p>默认: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m <span class="varname"> 標籤 </span> </span> </p> </td> 
  <td class="stentry"> <p>要求標籤；識別記錄檔中應播放的要求；規則運算式模式。 </p> <p>預設： <span class="codeph"> 要求： </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x <span class="varname"> 字尾 </span> </span> </p> </td> 
  <td class="stentry"> <p>要附加至從記錄檔擷取之要求的尾碼；可用來將播放的要求與記錄檔中的即時要求分開；「？」 或'&amp;'分隔符號會自動插入；字尾可參照任何記錄欄位（依位置在大括弧內），預設對應於md5簽名欄位。 </p> <p>預設： <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>詳細模式，將產生的請求URL列印到 <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h </span> </p> </td> 
  <td class="stentry"> <p>列印摘要至 <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method — 要使用的HTTP要求方法( <span class="codeph"> get|post|head|smart </span>)。 </p> <p>預設： <span class="codeph"> 智慧 </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos — 記錄檔中要從中抓取原始方法的位置。 </p> <p>預設： 15 </p> </td> 
 </tr> 
</table>

若是Windows，檔案名稱為 [!DNL playlog.bat] 在Linux上則是 [!DNL playlog.sh].

## 示例 {#section-716e5c35e9fa4ee3a4b0687381fcea40}

下列範例會播放「影像伺服」在Linux上建立的存取記錄檔中的所有請求：

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

下列命令會播放在「影像伺服」在Windows上建立的追蹤記錄檔中找到的所有要求：

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
