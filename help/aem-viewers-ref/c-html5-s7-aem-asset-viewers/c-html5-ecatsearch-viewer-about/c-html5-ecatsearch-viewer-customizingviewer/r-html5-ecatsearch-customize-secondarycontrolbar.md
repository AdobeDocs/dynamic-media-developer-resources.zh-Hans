---
title: 辅助控制栏
description: 辅助控制栏是包含“第一页”和“最后一页”按钮以及在CSS中可用时的“页面指示器”的矩形区域。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
TQID: 'https://experienceleague.adobe.com/NMaW0QPU2A3pUzpvMg3kbW8MmeLbJ1hZlCSGTEcG6Ko'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 171
ht-degree: 0%

---

# 辅助控制栏{#secondary-control-bar}

辅助控制栏是包含“第一页”和“最后一页”按钮以及在CSS中可用时的“页面指示器”的矩形区域。

默认情况下，该屏幕仅在手机上显示，位于查看器底部。 它始终占用整个可用查看器宽度。 可以通过CSS更改其相对于查看器容器的颜色、高度和垂直位置。

辅助控件栏的外观由以下CSS类选择器控制：

`.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p>位于查看器顶部。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">后</span> </p> </td> 
   <td colname="col2"> <p>位于查看器底部。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>主控制栏的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>辅助控制栏的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置一个高度为72像素且位于查看器容器底部的灰色辅助控件栏。

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```

