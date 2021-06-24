---
description: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog搜索
role: Developer,Business Practitioner
exl-id: 2669c8e2-c942-420f-8262-9d76d5c499a2
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

[!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *``*, *``*, *``*, *``*, *``*, *`dividerWidthdiverColordiverOpacityborderOnOffborderColorfillColor`*`]

在桌面系统上将[!DNL `PageView.frametransition`]设置为[!DNL `turn`]或[!DNL `auto`]时，控制组件外观。

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> diverWidth</span></span> </p> </td> 
   <td colname="col2"> <p> 分隔跨页中左和右页面的页面分隔阴影的宽度（以像素为单位）。 它还控制在车削页面旁边显示的运行阴影的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB格式的阴影颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p>在<span class="codeph"> 0</span>到<span class="codeph"> 1</span>的范围内的阴影不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> 打开和关闭在翻页周围的边框的标记（<span class="codeph"> 0</span>或<span class="codeph"> 1</span>）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB格式的边框颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> 在翻页动画期间使用的元件区域的实体填充的颜色（RRGGBB格式）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-54c634116cfe4f17813318e07539264c}

可选。

## 默认 {#section-43fd13f639c2480c82658fafeeaf0846}

[!DNL `40,909090,1,1,909090,FFFFFF`]

## 示例 {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`]
