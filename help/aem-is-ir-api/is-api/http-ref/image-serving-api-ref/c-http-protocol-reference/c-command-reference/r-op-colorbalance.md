---
description: 调整颜色平衡。 分别调整每个RGB颜色组件的值。
solution: Experience Manager
title: op_colorbalance
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 1%

---

# op_colorbalance{#op-colorbalance}

调整颜色平衡。 分别调整每个RGB颜色组件的值。

`op_colorbalance= *`redAdj`*, *`greenAdj`*, *`blueAdj`*`

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

灰度和CMYK输入图像数据使用简单转换转换为RGB，当启用色彩管理时，转换不准确。

## 属性 {#section-dff9c934f7c1442bbd02379b688d82e2}

“图层”命令。 应用于当前图层或复合图像，如果 `layer=comp`. 被效果层忽略。 在应用操作之前，CMYK图像和图层会转换为RGB。

## 默认 {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` 因为颜色没有变化。

## 示例 {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

将颜色平衡推向红色：

… `&op_colorBalance=100,0,0&`…
