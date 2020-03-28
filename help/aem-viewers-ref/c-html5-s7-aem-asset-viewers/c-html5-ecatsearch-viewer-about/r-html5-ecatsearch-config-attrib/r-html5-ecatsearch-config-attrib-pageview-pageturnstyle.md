---
description: 'null'
seo-description: 'null'
seo-title: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
topic: Dynamic media
uuid: 748adb73-bfb6-4fce-aa6a-4216184edabb
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.pageturnstyle{#pageview-pageturnstyle}

[!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *``*, *``*, *``*, *``*, *``*, *`dividerWidthdiverColordiverOpacityborderOnOffborderColorfillColor`*`]

在桌面系统上将组件设 [!DNL `PageView.frametransition`] 置为或设 [!DNL `turn`] 置为 [!DNL `auto`] 组件外观。

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> 分页阴影的宽度（以像素为单位），用于分隔跨页中的左页和右页。 它还控制在翻页旁边显示的正在运行的阴影的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB格式的阴影颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p>在0到1范围内的阴 <span class="codeph"> 影不透明</span><span class="codeph"> 度</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> 打开和关闭 <span class="codeph"> 翻页周围的边框的标</span> 志(0 <span class="codeph"> 或1</span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB格式的边框颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> 在翻页动画过程中使用的组件区域的实心填充颜色，采用RRGGBB格式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-54c634116cfe4f17813318e07539264c}

可选。

## 默认 {#section-43fd13f639c2480c82658fafeeaf0846}

[!DNL `40,909090,1,1,909090,FFFFFF`]

## 示例 {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`]
