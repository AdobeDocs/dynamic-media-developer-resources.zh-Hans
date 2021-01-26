---
description: 为公司定义发布目标。
seo-description: 为公司定义发布目标。
seo-title: PublishContext
solution: Experience Manager
title: PublishContext
topic: Dynamic Media Image Production System API
uuid: 62e2ba15-d966-48c7-86dc-373069c3ea46
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 18%

---


# PublishContext{#publishcontext}

为公司定义发布目标。

语法

## 参数 {#section-577d46cc75774c7c8fbdcff203a0d9ac}

资产会为每个发布状态和上下文保留一个单独的标记。 使用[setAssetsContextState](../../operations/c-operations-intro/c-methods/r-set-asset-context-state.md#reference-da96f9caef734f2883fddaf58cd886d7)设置发布状态。

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
   <td colname="col3">发布上下文的类型。 包括： 
    <ul id="ul_04CA7C755E5441AA8ABBD0BA3F245A78">
     <li id="li_7F578422D38E40D1A590AB21ADD84E90"><span class="codeph"> 图像服务</span></li>
     <li id="li_C112E12028E44ED7914ED0D3D6B3A45E"><span class="codeph"> 图像渲染</span></li>
     <li id="li_9430D600FA4343F6951F9AE8EA7F9530"><span class="codeph"> 视频</span></li>
     <li id="li_4122D853BE1B4ED3B412CFA7B659EB1D"><span class="codeph"> ServerDirectory</span></li>
    </ul></td>
  </tr>
 </tbody>
</table>

>[!MORELIKETHIS]
>
>* [发布上下文](../../string-constants/c-string-constants/r-publish-context.md#reference-3ade116df0df40deb86154eb0ac7c12a)

