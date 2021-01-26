---
description: 暗角文件。 指定要用于此请求的暗角。
seo-description: 暗角文件。 指定要用于此请求的暗角。
seo-title: 暗角
solution: Experience Manager
title: 暗角
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8bba4ad4-bd55-4c55-8ebf-585371cf33f1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 4%

---


# 暗角{#vignette}

暗角文件。 指定要用于此请求的暗角。

`vignette=[ *`catIdrecIdfile`*/] *``*|[catId/] *``*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>材料目录id（与<span class="codeph">属性：:RootId</span>匹配）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>暗角ID（与<span class="codeph">暗角：:Id</span>匹配）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 文件</span> </p></td> 
  <td class="stentry"> <p>相对暗角文件路径和名称。 </p></td> 
 </tr> 
</table>

可以指定暗角映射条目或暗角文件。 不允许使用远程URL。

`vignette=` 可用作在请求URL路径中指定暗角的替代方法。主要用于通过模板中的变量指定晕影。

如果未指定&#x200B;*`catId`*，则使用会话目录。

## 属性 {#section-f58661fc78d7496e8e3d0fb98b945c4b}

可能在请求中的任何位置发生。 覆盖使用请求URL路径指定的暗角。

## 默认 {#section-db0618d48bc84dc8abcc989550349ccc}

无。

## 另请参阅 {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[材料目录](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)，自 [定义变量](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
