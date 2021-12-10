---
title: PageView.frametransition
description: PageView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026c2fc5-0460-481c-aca9-ddd25371779c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 5%

---

# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`时段`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幻灯片|转弯|自动</span> </p> </td> 
   <td colname="col2"> <p> 指定对帧更改应用的效果类型。 </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> 幻灯片</span> 激活一个过渡，其中旧框架滑出视图，而新框架滑入到视图中。 </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> 转弯</span> 当用户可以拖动四个跨页角之一并执行交互式页面翻转时，会启用页面翻转效果。 </p> <p>When <span class="codeph"> 转弯</span> 使用 <span class="codeph"> pageturnstyle</span> 修饰符和 <span class="codeph"> .s7pagedifier</span> 将忽略CSS类。 </p> <p>注意︰  <p><span class="codeph"> 转弯</span> Motorola Xoom不支持动画。 </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> 自动</span> 在台式机系统上设置转弯框架过渡，在触控设备上设置滑动过渡。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 时段</span></span> </p> </td> 
   <td colname="col2"> <p>指定的持续时间（以秒为单位） <span class="codeph"> 幻灯片</span> 或 <span class="codeph"> 转弯</span> 过渡效果。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-4d25a3f483834d2b9586fa70270ce6bd}

可选。

## 默认 {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## 示例 {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
