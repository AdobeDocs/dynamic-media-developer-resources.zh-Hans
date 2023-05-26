---
title: InfoPanelPopup.infoServerUrl
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 83abaecb-cc85-4918-98ed-2770b4ca407b
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>信息服务器URL模板用于获取信息面板内容模板中变量替换的键/值对。 指定的模板通常包含宏占位符，这些占位符在请求发送到服务器之前被替换为实际数据。 </p> <p><span class="codeph"> $1$</span> 替换为触发的变换值 <span class="codeph"> InfoPanelPopup</span> 激活。 </p> <p><span class="codeph"> $2$</span> 替换为图像集中当前帧的序列号。 </p> <p><span class="codeph"> $3$</span> 替换为当前项目的父集名称中指定的第一个路径元素。 它通常对应于目录ID。 </p> <p><span class="codeph"> $4$</span> 替换为路径中的以下元素，并与资产id相对应。 实际的信息服务器请求语法取决于信息服务器，并且因服务器而异。 例如，以下是典型的Dynamic Media info server请求模板： </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
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
