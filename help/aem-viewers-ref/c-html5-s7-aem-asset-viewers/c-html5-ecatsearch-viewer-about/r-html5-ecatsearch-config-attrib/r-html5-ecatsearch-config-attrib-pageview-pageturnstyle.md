---
description: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2669c8e2-c942-420f-8262-9d76d5c499a2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

[!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *`分隔线宽度`*, *`分隔线颜色`*, *`分隔线不透明度`*, *`borderOnOff`*, *`borderColor`*, *`填充颜色`*`]

控制组件外观，当 [!DNL `PageView.frametransition`] 设置为 [!DNL `turn`] 或 [!DNL `auto`] 在桌面系统上。

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 分隔线宽度</span></span> </p> </td> 
   <td colname="col2"> <p> 跨页中分隔左右页面的页面分隔线阴影的宽度（以像素为单位）。 它还控制车削页面旁边显示的运行阴影的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 分隔线不透明度</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB格式的阴影颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 分隔线不透明度</span></span> </p> </td> 
   <td colname="col2"> <p>范围内的阴影不透明度 <span class="codeph"> 0</span> 到 <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> 标志(或 <span class="codeph"> 0</span> 或 <span class="codeph"> 1</span>)来打开和关闭打开页面周围的边框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB格式的边框颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 填充颜色</span></span> </p> </td> 
   <td colname="col2"> <p> 翻页动画期间使用的组件区域的纯色填充颜色（RRGGBB格式）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-54c634116cfe4f17813318e07539264c}

可选.

## 默认 {#section-43fd13f639c2480c82658fafeeaf0846}

[!DNL `40,909090,1,1,909090,FFFFFF`]

## 示例 {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`]
