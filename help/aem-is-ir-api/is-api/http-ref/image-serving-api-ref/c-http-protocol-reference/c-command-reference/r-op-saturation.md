---
description: 调整饱和度。 更改图层或复合图像的每个可见像素的饱和度。
solution: Experience Manager
title: op_saturation
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---


# op_saturation{#op-saturation}

调整饱和度。 更改图层或复合图像的每个可见像素的饱和度。

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>饱和度调整(-100...+100 int)。 </p></td> 
 </tr> 
</table>

`op_saturation=-100` 使图像完全失色。

## 属性 {#section-9a3cc9ff060049449554dfa69d92fd53}

图层命令。 应用于当前图层或复合图像（如果`layer=comp`）。 被效果图层忽略。

## 默认 {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`，以保持饱和度不变。在应用操作之前，CMYK图像或图层将转换为RGB。

## 示例 {#section-033b272f1b7e4efeb94e841fd8095357}

处理彩色照片以获得“高调”外观：

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
