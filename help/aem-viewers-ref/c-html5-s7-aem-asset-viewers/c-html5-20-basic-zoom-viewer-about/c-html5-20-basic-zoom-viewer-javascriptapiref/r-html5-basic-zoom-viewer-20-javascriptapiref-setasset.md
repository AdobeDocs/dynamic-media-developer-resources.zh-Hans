---
title: setAsset
description: 基本缩放查看器的JavaScript API引用。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 71525aac-b8ca-4f5a-a770-268857ddae4f
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 3%

---

# setAsset{#setasset}

基本缩放查看器的JavaScript API引用。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 资产</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> 字符串</span>}新资产id，并在“？”后面附加可选的IS修饰符 </p> <p> 此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

设置新资产。 您可以在之前或之后随时调用此参数 `init()`. 如果在 `init()`，则查看器会在运行时交换资产。

另请参阅 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

单个图像引用：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

锐化修饰符已添加到该集中的所有图像：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B?op_sharpen=1")
```
