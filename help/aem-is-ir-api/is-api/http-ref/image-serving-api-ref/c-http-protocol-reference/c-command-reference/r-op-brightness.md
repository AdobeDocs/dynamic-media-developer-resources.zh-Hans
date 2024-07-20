---
title: op_亮度
description: 调整亮度。 降低或增加图像亮度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 390ed812-87ae-41e7-8021-65dd95915ae8
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 2%

---

# op_亮度{#op-brightness}

调整亮度。 降低或增加图像亮度。

`op_brightness= *`调整`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">调整</span> </p> </td> 
  <td class="stentry"> <p>亮度调整(-100...+100 int)。 </p></td> 
 </tr> 
</table>

## 属性 {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

图层命令。 应用于当前图层或复合图像（如果`layer=comp`）。 被效果层忽略。 在应用操作之前，CMYK图像或图层将转换为RGB。

## 默认 {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`，表示亮度不变。

## 示例 {#section-c25f952f1b77409abb9ccf885862d75c}

略微使图像的背景变暗以强调前景内容：

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
