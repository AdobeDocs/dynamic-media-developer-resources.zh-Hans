---
description: 视图宽度。 指定回复图像（视图图像）的宽度。
solution: Experience Manager
title: wid
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---

# wid{#wid}

视图宽度。 指定回复图像（视图图像）的宽度。

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>图像宽度（以像素为单位，int大于0）， </p></td> 
 </tr> 
</table>

## 默认 {#section-830bae0b6bac440098444d7cdcb23e2e}

如果两者都不 `wid=`， `hei=`，也不 `scale=` 指定时，回复图像是FXG文件中指定的默认视图大小。

栅格格式使用“默认视图大小”（或DefaultPix设置）渲染。 单击 **[!UICONTROL 应用程序设置]** > **[!UICONTROL 发布设置]** > **[!UICONTROL 图像服务器]**，然后输入宽度和高度值。 尺寸越小，性能越好。 您必须保存设置并执行图像服务发布以应用更改。

如果您应用 `scale=1` 命令，栅格格式请求将以FXG中指定的大小呈现。

## 示例 {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

除非指定格式，否则图像将渲染为SWF文件。 在这种情况下，高度和宽度没有意义，因为SWF通常会扩展至浏览器窗口的大小。 因此，hei和wid仅适用于光栅或PDF格式。 栅格格式包括：

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIFalpha
* tif-alpha
* png-alpha
