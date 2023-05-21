---
description: 「影像伺服」來源資料檔案包含影像和遮色片檔案、字型和ICC設定檔。
solution: Experience Manager
title: 來源資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# 來源資料{#source-data}

「影像伺服」來源資料檔案包含影像和遮色片檔案、字型和ICC設定檔。

影像伺服器必須能夠存取所有來源資料檔案。 「影像伺服」提供許多指定資料檔案位置的替代方式：

`*`install_folder`*/ *`rootPath`*/ *`檔案路徑`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS：：RootPath/attribute：：RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 檔案路徑 </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 目錄路徑</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog：：Path|catalog：：MaskPath|icc：：ProfilePath|font：：FontPath|font：：MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 請求路徑</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 影像伺服HTTP請求中指定的相對影像檔案路徑和名稱</span> </p></td> 
 </tr> 
</table>

伺服器會由右至左組合路徑區段，直到建立絕對檔案路徑為止。

全部 `*`rootPath`*` 區段可以是空白、相對或絕對路徑區段。

`*`目錄路徑`*` 是絕對或相對檔案路徑/名稱。 `*`請求路徑`*` 必須為相對檔案路徑/名稱。

`Multiple IS::RootPath` 值可在ImageServerRegistry.xml中定義（或透過管理介面定義）。 如此一來，來源資料檔案便能分散到多個檔案系統中。 影像伺服器將嘗試以指定的順序替代路徑，直到找到資料檔案為止。

任何型別的新資料檔案都可隨時新增，不需停止伺服器。
