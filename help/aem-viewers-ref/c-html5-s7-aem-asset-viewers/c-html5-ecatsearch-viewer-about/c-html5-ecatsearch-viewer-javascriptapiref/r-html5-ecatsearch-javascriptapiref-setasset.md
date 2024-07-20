---
description: 视频查看器的JavaScript API参考。
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 5fd80f8d-321e-47f4-9fb2-65e7bd63be58
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 1%

---

# setAsset{#setasset}

视频查看器的JavaScript API参考。

[!DNL ` setAsset( *`资源`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">资源</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph">字符串</span>}新资产ID或在<span class="codeph">后附加可选图像服务修饰符的显式图像集？</span>。 </p> <p> 此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

设置新资源。 您可以随时在[!DNL `init()`]之前或之后调用此参数。 如果在[!DNL `init()`]之后调用，则查看器会在运行时交换资源。

另请参阅[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

对目录中定义的图像集的单个引用：

```
 <instance>.setAsset("Viewers/Pluralist")
```

显式图像集，带有预组合的页面：

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

明确的图像集，包含各个页面图像：

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

向集中的所有图像添加了锐化修饰符：

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```
