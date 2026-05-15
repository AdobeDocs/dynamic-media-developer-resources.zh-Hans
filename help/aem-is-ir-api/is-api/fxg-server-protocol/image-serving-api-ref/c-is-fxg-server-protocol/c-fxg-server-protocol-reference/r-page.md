---
title: 页面
description: 检索页面。 在多页FXG中检索特定页面。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c72ceff-30d9-4e0b-8b4f-6cb0039d389e
TQID: 'https://experienceleague.adobe.com/-YFn2qqG1ZfEQKVdQojrnYlgkCjIxvSxCJ-IKxs2gZI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 52
ht-degree: 5%

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
