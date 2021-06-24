---
description: 检索页面。 检索多页面FXG中的特定页面。
solution: Experience Manager
title: 页面
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 7c72ceff-30d9-4e0b-8b4f-6cb0039d389e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 5%

---

# 页面{#page}

检索页面。 检索多页面FXG中的特定页面。

`page= *`val`*`

<table id="simpletable_E92560F812B64A36A3D108CA7DEED5AC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>页码（第一页为1）。 </p></td> 
 </tr> 
</table>

## 默认 {#section-3fd7fcc525b947c7a95457e50414ac9e}

如果未指定`page`，则为光栅输出返回第一页，为PDF输出返回所有页。
