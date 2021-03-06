---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog搜索
role: Developer,User
exl-id: f4bb0087-1e49-47e2-84b4-44b92fade36a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>信息服务器URL模板用于获取信息面板内容模板中变量替换的键/值对。指定的模板通常包含宏占位符，在将请求发送到服务器之前，宏占位符会被替换为实际数据。 </p> <p><span class="codeph"> $1$</span> 将被触发InfoPanelPopupactivation的滚动值替 <span class="codeph"> </span> 换。 </p> <p><span class="codeph"> $2$</span> 将替换为图像集中当前帧的序列号。 </p> <p><span class="codeph"> $3$</span> 将被替换为在当前项目父项集名称中指定的第一个路径元素。它通常与目录ID相对应。 </p> <p><span class="codeph"> $4$</span> 将在路径中替换为以下元素，并与资产id相对应。实际的信息服务器请求语法与信息服务器相关，它不同于服务器。 例如，以下是典型的Dynamic Media信息服务器请求模板： </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>请注意，配置“信息面板弹出窗口”时，传递到“信息面板”的HTML代码和JavaScript代码将在客户端的计算机上运行。 因此，请确保此类HTML代码和JavaScript代码的安全。

## 属性 {#section-71356e3c13244e62b0582980d9d05328}

可选。

## 默认 {#section-22e9af803f724434807d34e200eb7518}

无。

## 示例 {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
