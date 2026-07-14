---
title: 標幟
description: 应用标志。 指定其他渲染选项。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
TQID: 'https://experienceleague.adobe.com/tdbtQIxutlPSPRm4vGWCQLM8veyivWfabKos9YbvfYg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 4%

---

# 標幟 {#flags}

应用标志。 指定其他渲染选项。

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">值</span> </p> </td> 
  <td class="stentry"> <p>标志值。 </p></td> 
 </tr> 
</table>

目前仅用于机箱材料。

`flags=0` （默认）呈现带有实心门的上文件柜。

`flags=1`呈现带有玻璃门的上柜（如果晕影是用玻璃门创作的）。

## 属性 {#section-a2b00d7bb15e449ea85178acb92d8285}

材质属性。 如果不是机箱材料，或者目标机箱对象不允许玻璃门，则忽略此项。

## 默认 {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0`无玻璃门。

