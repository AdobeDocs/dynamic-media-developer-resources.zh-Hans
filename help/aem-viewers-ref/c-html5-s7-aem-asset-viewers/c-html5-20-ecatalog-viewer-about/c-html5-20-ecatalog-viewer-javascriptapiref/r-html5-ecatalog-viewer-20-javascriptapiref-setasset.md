---
description: 视频查看器的JavaScript API参考。
seo-description: 视频查看器的JavaScript API参考。
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic Media
uuid: b95cef30-41ad-47d5-b0f1-efc8831c7bdc
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---


# setAsset{#setasset}

视频查看器的JavaScript API参考。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 资产  </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph">字符串</span>}新资产id或显式图像集，并在<span class="codeph">后附加可选的图像服务修饰符？</span>。 </p> <p> 此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

设置新资产。 您可以随时在`init()`之前或之后调用此参数。 如果在`init()`之后调用它，则查看器会在运行时交换资产。

另请参阅[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

对在目录中定义的图像集的单个引用：

```
 <instance>.setAsset("Viewers/Pluralist")
```

显式图像集，预组合页面：

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

显式图像集，包含单个页面图像：

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

锐化修饰符已添加到该集中的所有图像：

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```

