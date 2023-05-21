---
description: 定義公司的發佈目標。
solution: Experience Manager
title: PublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b0656d6c-0f73-4f1d-9e1f-20b07cfe44b9
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 17%

---

# [!DNL PublishContext]{#publishcontext}

定義公司的發佈目標。

语法

## 参数 {#section-577d46cc75774c7c8fbdcff203a0d9ac}

資產會為各個發佈狀態和內容維護個別的標籤。 設定發佈狀態 [setAssetsContextState](../../operations/c-operations-intro/c-methods/r-set-asset-context-state.md#reference-da96f9caef734f2883fddaf58cd886d7).

<table id="table_1165D5DDC89140CD8222E5A04B39048E">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 名称 </th>
   <th colname="col2" class="entry"> 类型 </th>
   <th colname="col3" class="entry"> 说明 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextHandle</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string </span></td>
   <td colname="col3"> 處理發佈內容的動作。 </td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextName</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string</span></td>
   <td colname="col3"> 發佈內容的名稱。 </td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextType</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string</span></td>
   <td colname="col3">發佈內容的型別。 包括： 
    <ul id="ul_04CA7C755E5441AA8ABBD0BA3F245A78">
     <li id="li_7F578422D38E40D1A590AB21ADD84E90"><span class="codeph"> ImageServe</span></li>
     <li id="li_C112E12028E44ED7914ED0D3D6B3A45E"><span class="codeph"> 影像演算</span></li>
     <li id="li_9430D600FA4343F6951F9AE8EA7F9530"><span class="codeph"> 视频</span></li>
     <li id="li_4122D853BE1B4ED3B412CFA7B659EB1D"><span class="codeph"> 伺服器目錄</span></li>
    </ul></td>
  </tr>
 </tbody>
</table>

>[!MORELIKETHIS]
>
>* [發佈內容](../../string-constants/c-string-constants/r-publish-context.md#reference-3ade116df0df40deb86154eb0ac7c12a)

