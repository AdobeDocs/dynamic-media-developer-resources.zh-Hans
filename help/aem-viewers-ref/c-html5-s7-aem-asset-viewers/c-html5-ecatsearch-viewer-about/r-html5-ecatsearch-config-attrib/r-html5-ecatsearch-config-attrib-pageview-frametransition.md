---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 19239fa8-65a8-487f-9370-42bb93d862d5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`持续时间`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幻灯片|翻转|自动</span> </p> </td> 
   <td colname="col2"> <p> 指定对帧更改应用的效果的类型。 </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph">幻灯片</span>激活旧框架滑出视图和新框架滑入视图的过渡。 </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph">翻转</span>可启用页面翻转效果，此时用户可以拖动四个跨页角之一并执行交互式页面翻转。 </p> <p>使用<span class="codeph"> turn</span>时，组件的外观通过<span class="codeph"> pageturnstyle</span>修饰符进行控制，并忽略<span class="codeph"> .s7pagedivider</span> CSS类。 </p> <p>注意︰  <p>摩托罗拉Xoom不支持<span class="codeph">翻转</span>动画。 </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span>在桌面系统上设置turn frame过渡，在触控设备上设置slide过渡。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">持续时间</span></span> </p> </td> 
   <td colname="col2"> <p>指定<span class="codeph">幻灯片</span>或<span class="codeph">转换</span>效果的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-4d25a3f483834d2b9586fa70270ce6bd}

可选.

## 默认 {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## 示例 {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
