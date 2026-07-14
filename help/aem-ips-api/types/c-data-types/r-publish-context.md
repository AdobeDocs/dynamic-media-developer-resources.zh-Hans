---
description: 为公司定义发布目标。
solution: Experience Manager
title: Publishcontext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b0656d6c-0f73-4f1d-9e1f-20b07cfe44b9
TQID: 'https://experienceleague.adobe.com/BrMmLNSGcve-w8clATFAiVSVNI8CTQGXYA6ydnIDUzg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 64
ht-degree: 14%

---

# [!DNL PublishContext]{#publishcontext}

为公司定义发布目标。

语法

## 参数 {#section-577d46cc75774c7c8fbdcff203a0d9ac}

Assets为每个发布状态和上下文维护一个单独的标记。 使用[setAssetsContextState](../../operations/c-operations-intro/c-methods/r-set-asset-context-state.md#reference-da96f9caef734f2883fddaf58cd886d7)设置发布状态。

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
   <td colname="col3"> 处理发布上下文。 </td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextName</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string</span></td>
   <td colname="col3"> 发布上下文的名称。 </td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextType</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string</span></td>
   <td colname="col3">发布上下文的类型。 包括： <ul id="ul_04CA7C755E5441AA8ABBD0BA3F245A78">
     <li id="li_7F578422D38E40D1A590AB21ADD84E90"><span class="codeph"> Imageserving</span></li>
     <li id="li_C112E12028E44ED7914ED0D3D6B3A45E"><span class="codeph"> ImageRendering</span></li>
     <li id="li_9430D600FA4343F6951F9AE8EA7F9530"><span class="codeph"> 视频</span></li>
     <li id="li_4122D853BE1B4ED3B412CFA7B659EB1D"><span class="codeph"> 服务器目录</span></li>
    </ul></td>
  </tr>
 </tbody>
</table>

>[!MORELIKETHIS]
>
>* [发布上下文](../../string-constants/c-string-constants/r-publish-context.md#reference-3ade116df0df40deb86154eb0ac7c12a)

