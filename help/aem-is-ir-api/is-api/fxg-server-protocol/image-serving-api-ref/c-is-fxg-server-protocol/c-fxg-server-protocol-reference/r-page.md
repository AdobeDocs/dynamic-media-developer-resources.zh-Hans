---
description: 检索页面。 检索多页FXG中的特定页面。
seo-description: 检索页面。 检索多页FXG中的特定页面。
seo-title: 页面
solution: Experience Manager
title: 页面
topic: Scene7 Image Serving - Image Rendering API
uuid: 3379c8d8-6e2e-4bd5-b683-a532330f1ddc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 页面{#page}

检索页面。 检索多页FXG中的特定页面。

`page= *`val`*`

<table id="simpletable_E92560F812B64A36A3D108CA7DEED5AC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>页码（第一页为1）。 </p></td> 
 </tr> 
</table>

## 默认 {#section-3fd7fcc525b947c7a95457e50414ac9e}

如果 `page` 未指定，则为栅格输出返回第一页，为PDF输出返回所有页。
