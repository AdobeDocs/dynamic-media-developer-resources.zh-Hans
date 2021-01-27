---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
topic: Dynamic Media
uuid: 12595a89-bad5-4224-aeff-52ce6bb615ee
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 5%

---


# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`时段`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幻灯片|转换|自动</span> </p> </td> 
   <td colname="col2"> <p> 指定对帧更改应用的效果类型。 </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> 幻</span> 灯片激活过渡，旧帧滑出视图，新帧滑入视图。 </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> 当</span> 用户可拖动四个跨页角之一并执行交互式页面翻转时，可启用页面翻转效果。 </p> <p>当使用<span class="codeph"> turn</span>时，使用<span class="codeph"> pageturnstyle</span>修饰符控制组件的外观，并忽略<span class="codeph"> .s7pagedivider</span> CSS类。 </p> <p>注意︰  <p><span class="codeph"> Motorola </span> Xoom不支持turnanimation。 </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> 在桌</span> 面系统上自动设置转弯框过渡，在触控设备上自动设置幻灯片过渡。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 时段</span></span> </p> </td> 
   <td colname="col2"> <p>指定<span class="codeph">幻灯片</span>或<span class="codeph"> turn</span>过渡效果的持续时间（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-4d25a3f483834d2b9586fa70270ce6bd}

可选。

## 默认 {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## 示例 {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
