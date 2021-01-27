---
description: 交互式视频查看器的配置属性。
seo-description: 交互式视频查看器的配置属性。
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic Media
uuid: b3978280-7826-44c0-bd25-357e145121f8
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

交互式视频查看器的配置属性。

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> 指定按钮容器的幻灯片动画方向。 当设置为<span class="codeph"> up</span>、<span class="codeph"> down</span>、<span class="codeph"> left</span>或<span class="codeph"> right</span>时，面板将沿指定方向滚出，而不进行任何额外的边界检查，这可能导致面板被外部容器夹住。 </p> <p>当设置为<span class="codeph"> fit-vertical</span>时，组件首先将基板位置移至SocialShare的底部，并尝试从此基本位置沿下列方向之一展开面板：下，右，左。 每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试都失败，则组件会尝试将基板位置移到顶部，并从顶部、右侧和左侧重复滚出尝试。 </p> <p>当设置为<span class="codeph"> fit-lateral</span>时，组件使用类似的逻辑，但首先将基向右移动，然后向右、向下和向上转出方向。 然后，它把基向左移动，尝试左、下和上移方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```

