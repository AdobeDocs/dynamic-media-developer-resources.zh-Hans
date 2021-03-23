---
description: 调整色彩平衡。 单独调整每个RGB颜色分量的值。
seo-description: 调整色彩平衡。 单独调整每个RGB颜色分量的值。
seo-title: op_colorbalance
solution: Experience Manager
title: op_colorbalance
uuid: 177aa6e3-1b32-4254-85f1-d7fe14116e3c
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---


# op_colorbalance{#op-colorbalance}

调整色彩平衡。 单独调整每个RGB颜色分量的值。

`op_colorbalance= *``*, *``*, *`redAdjgreenAdjblueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>红色分量调整(-100...+100 int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>绿色组件调整(-100...+100 int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>蓝色分量调整(-100...+100 int)。 </p></td> 
 </tr> 
</table>

灰色和CMYK输入图像数据使用朴素转换转换为RGB，这在启用色彩管理时是不准确的。

## 属性 {#section-dff9c934f7c1442bbd02379b688d82e2}

图层命令。 应用于当前图层或复合图像（如果`layer=comp`）。 被效果图层忽略。 在应用操作之前，CMYK图像和图层将转换为RGB。

## 默认 {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` 不会改变颜色。

## 示例 {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

将色彩平衡推向红色：

… `&op_colorBalance=100,0,0&`…
