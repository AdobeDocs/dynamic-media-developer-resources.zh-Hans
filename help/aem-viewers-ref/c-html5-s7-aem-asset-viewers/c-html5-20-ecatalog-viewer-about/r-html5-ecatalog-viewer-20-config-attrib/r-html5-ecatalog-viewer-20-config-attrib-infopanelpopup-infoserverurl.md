---
title: InfoPanelPopup.infoServerUrl
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 83abaecb-cc85-4918-98ed-2770b4ca407b
TQID: 'https://experienceleague.adobe.com/AFeptUljCobQmP2KN2Cx-F-gddObD-AgDJznC5oVdes'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>信息服务器URL模板用于在信息面板内容模板中为变量替换获取键/值对。 指定的模板通常包含宏占位符，在请求发送到服务器之前，这些占位符会替换为实际数据。 </p> <p><span class="codeph"> $1$</span>被替换为触发<span class="codeph"> InfoPanelPopup</span>激活的变换值。 </p> <p><span class="codeph"> $2$</span>被替换为图像集中当前帧的序列号。 </p> <p><span class="codeph"> $3$</span>被替换为当前项的父集名称中指定的第一个路径元素。 它通常对应于目录ID。 </p> <p><span class="codeph"> $4$</span>在路径中被替换为以下元素，并与资产ID相对应。 实际的信息服务器请求语法依赖于信息服务器，并且它因服务器而异。 例如，以下是典型的Dynamic Media信息服务器请求模板： </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>配置信息面板弹出窗口时，传递到信息面板的HTML代码和JavaScript代码将在客户端计算机上运行。 因此，请确保此类HTML代码和JavaScript代码是安全的。

## 属性 {#section-71356e3c13244e62b0582980d9d05328}

可选.

## 默认 {#section-22e9af803f724434807d34e200eb7518}

无。

## 示例 {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`
