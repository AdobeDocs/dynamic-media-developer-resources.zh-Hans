---
description: 'null'
seo-description: 'null'
seo-title: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
topic: Dynamic media
uuid: feeb02c0-f3f9-4559-acd9-cad30788b70b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`时段`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幻灯片|旋转|自动</span> </p> </td> 
   <td colname="col2"> <p> 指定应用于帧更改的效果类型。 </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> slide</span> 激活过渡，旧帧滑出视图，新帧滑入视图。 </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> turn</span> 在用户可以拖动四个跨页角之一并执行交互式页面翻转时启用页面翻转效果。 </p> <p>使 <span class="codeph"> 用Turn</span> 时，组件的外观由pageturnstyle修饰符控制 <span class="codeph"> ，并忽略</span> .s7pagedivider <span class="codeph"></span> CSS类。 </p> <p>注意︰  <p><span class="codeph"> Motorola</span> Xoom不支持旋转动画。 </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> 自动</span> 设置桌面系统上的转换帧过渡和触控设备上的幻灯片过渡。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 时段</span></span> </p> </td> 
   <td colname="col2"> <p>指定幻灯片或旋转 <span class="codeph"> 过渡效果</span> ，以 <span class="codeph"></span> 秒为单位。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-4d25a3f483834d2b9586fa70270ce6bd}

可选。

## 默认 {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## 示例 {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
