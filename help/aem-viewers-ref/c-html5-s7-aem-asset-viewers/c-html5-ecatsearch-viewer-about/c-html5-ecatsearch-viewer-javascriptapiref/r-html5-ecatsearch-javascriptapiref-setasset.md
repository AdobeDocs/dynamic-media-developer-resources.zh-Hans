---
description: 视频查看器的JavaScript API引用。
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog搜索
role: Developer,User
exl-id: 5fd80f8d-321e-47f4-9fb2-65e7bd63be58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# setAsset{#setasset}

视频查看器的JavaScript API引用。

[!DNL ` setAsset( *`asset`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 资产  </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph">字符串</span>}新资产id或显式图像集，其中的可选图像服务修饰符附加在<span class="codeph">之后？</span>。 </p> <p> 此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

设置新资产。 您可以在[!DNL `init()`]之前或之后随时调用此参数。 如果在[!DNL `init()`]之后调用，则查看器在运行时会交换资产。

另请参阅[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

对目录中定义的图像集的单个引用：

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
