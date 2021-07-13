---
description: 视图宽度。 指定回复图像（查看图像）的宽度。
solution: Experience Manager
title: wid
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 3%

---

# wid{#wid}

视图宽度。 指定回复图像（查看图像）的宽度。

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>图像宽度（以像素为单位，整数大于0）， </p></td> 
 </tr> 
</table>

## 默认 {#section-830bae0b6bac440098444d7cdcb23e2e}

如果既未指定`wid=`、`hei=`和`scale=`，则回复图像为FXG文件中指定的默认视图大小。

栅格格式使用“默认视图大小”（或“默认图像”设置）呈现。 单击&#x200B;**[!UICONTROL 应用程序设置]** > **[!UICONTROL 发布设置]** > **[!UICONTROL 图像服务器]**，然后输入宽度和高度值。 较小的尺寸可提供更好的性能。 您必须保存设置并执行图像提供发布以应用更改。

如果应用`scale=1`命令，将以FXG中指定的大小呈现光栅格式请求。

## 示例 {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

除非指定格式，否则图像将呈现为SWF文件。 在这种情况下，高度和宽度没有任何意义，因为SWF通常会扩展为浏览器窗口的大小。 因此，hei和wid仅适用于光栅格式或PDF格式。 光栅格式包括：

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-α
* PNG-α
