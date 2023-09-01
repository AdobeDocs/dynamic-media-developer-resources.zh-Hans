---
title: hei
description: 视图高度。 指定回复图像的高度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 2%

---

# hei{#hei}

视图高度。 指定回复图像的高度。

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>图像高度，以像素为单位（int大于0）。 </p></td> 
 </tr> 
</table>

栅格格式使用“默认视图大小”（或DefaultPix设置）渲染。 选择 **[!UICONTROL 应用程序设置]** > **[!UICONTROL 发布设置]** > **[!UICONTROL 图像服务器]**，然后输入宽度和高度值。 尺寸越小，性能越高。 保存设置并执行图像服务发布以应用更改。

如果您应用 `scale=1` 命令，栅格格式请求将以FXG中指定的大小呈现。

## 默认 {#section-76ee3daa77cb468ab310821357cc9404}

如果 `wid=`， `hei=`，或 `scale=` 未指定，回复图像是FXG文件中指定的默认视图大小。

## 示例 {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

除非指定格式，否则图像将渲染为SWF文件。 在这种情况下，高度和宽度没有意义，因为SWF通常会扩展到浏览器窗口的大小。 因此，其和wid仅适用于光栅或PDF格式。 栅格格式包括：

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* tif-alpha
* png-alpha
