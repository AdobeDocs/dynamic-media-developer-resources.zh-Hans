---
title: 页面
description: 检索页面。 在多页FXG中检索特定页面。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c72ceff-30d9-4e0b-8b4f-6cb0039d389e
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 6%

---

# 页面{#page}

检索页面。 在多页FXG中检索特定页面。

`page= *`val`*`

<table id="simpletable_E92560F812B64A36A3D108CA7DEED5AC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">值</span></span> </p> </td> 
  <td class="stentry"> <p>页码（第一页为1）。 </p></td> 
 </tr> 
</table>

## 默认 {#section-3fd7fcc525b947c7a95457e50414ac9e}

如果未指定`page`，则为光栅输出返回第一页，为PDF输出返回所有页。
