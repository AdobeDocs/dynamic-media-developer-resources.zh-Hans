---
description: 视图宽度。 指定回复图像(视图图像)的宽度。
seo-description: 视图宽度。 指定回复图像(视图图像)的宽度。
seo-title: wid
solution: Experience Manager
title: wid
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b59b936c-abab-4f9d-95ca-0a09743ba0fb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 4%

---


# wid{#wid}

视图宽度。 指定回复图像(视图图像)的宽度。

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>图像宽度（以像素为单位，int大于0）, </p></td> 
 </tr> 
</table>

## 默认 {#section-830bae0b6bac440098444d7cdcb23e2e}

如果既未指定`wid=`、`hei=`和`scale=`，则返回图像是FXG文件中指定的默认视图大小。

栅格格式使用“默认视图大小”（或“DefaultPix”设置）进行渲染。 单击&#x200B;**[!UICONTROL 应用程序设置]** > **[!UICONTROL 发布设置]** > **[!UICONTROL 图像服务器]**，然后输入宽度和高度值。 较小的尺寸可提供更好的性能。 要应用更改，必须保存设置并执行图像服务发布。

如果应用`scale=1`命令，则栅格格式请求将以FXG中指定的大小呈现。

## 示例 {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

除非指定格式，否则图像将呈现为SWF文件。 在这种情况下，高度和宽度毫无意义，因为SWF通常会扩展到浏览器窗口的大小。 因此，hei和wid仅适用于栅格或PDF格式。 栅格格式包括：

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-α
* PNG-alpha

