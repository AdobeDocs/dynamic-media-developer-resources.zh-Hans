---
description: 弹出查看器的JavaScript API引用。
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic，查看器，SDK/API，弹出
role: Developer,User
exl-id: cd66267e-7b25-4af4-b83c-f7b7f768ea8c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 2%

---

# setAsset{#setasset}

弹出查看器的JavaScript API引用。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 资产</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph">字符串</span>}个新资产id、显式图像集或显式图像集（包含特定于帧的图像服务修饰符），以及可选的全局图像服务修饰符（附加在<span class="codeph"> ?</span>之后）。 </p> <p> 此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

设置新资产。 您可以在`init()`之前或之后随时调用此参数。 如果在`init()`之后调用，则查看器在运行时会交换资产。

另请参阅[init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463)。

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

单个图像引用：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

对目录中定义的图像集的单个引用：

```
<instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

显式图像集：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

使用特定于帧的图像服务修饰符的显式图像集：

```
<instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

锐化修饰符已添加到该集中的所有图像：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```
