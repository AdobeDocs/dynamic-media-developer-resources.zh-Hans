---
title: 晕影
description: 晕影文件。 指定用于请求的晕影。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8419d68d-7579-4e62-abbd-7dc0a736ae23
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---

# 晕影{#vignette}

晕影文件。 指定用于请求的晕影。

`vignette=[ *`catId`*/] *`recId`*|[catId/] *`文件`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>材料目录ID(匹配 <span class="codeph"> attribute：：RootId</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>晕影ID(匹配 <span class="codeph"> 晕影：：Id</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 文件</span> </p></td> 
  <td class="stentry"> <p>相对晕影文件路径和名称。 </p></td> 
 </tr> 
</table>

可以指定晕影映射条目或晕影文件。 不允许使用远程URL。

`vignette=` 可用作在请求URL路径中指定晕影的替代方法。 用于通过模板中的变量指定晕影。

如果 *`catId`* 未指定，将使用会话目录。

## 属性 {#section-f58661fc78d7496e8e3d0fb98b945c4b}

可能出现在请求中的任何位置。 覆盖使用请求URL路径指定的晕影。

## 默认 {#section-db0618d48bc84dc8abcc989550349ccc}

无。

## 另请参阅 {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[物料目录](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)， [自定义变量](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
