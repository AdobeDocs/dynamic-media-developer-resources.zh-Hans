---
description: 将图像保存到文件。
seo-description: 将图像保存到文件。
seo-title: saveToFile
solution: Experience Manager
title: saveToFile
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 32a56d77-89e2-4f78-9fab-1b528e9a024a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---


# saveToFile{#savetofile}

将图像保存到文件。

`req=saveToFile&name= *``*[&timeout= *`fileval`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 文件</span> </p> </td> 
  <td class="stentry"> <p>目标图像文件的相对路径。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>超时时间间隔（毫秒）。 </p></td> 
 </tr> 
</table>

将响应映像保存到服务器上的文件，而不是返回到客户端。

当保存请求成功完成时，该请求返回多个Java格式的属性，包括：

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 属性</b> </th> 
   <th class="entry"> <b> 类型</b> </th> 
   <th class="entry"> <b> 说明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> lastUpdated</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>文件创建时间（自1970年UTC/GMT年1月1日午夜以来的毫秒数）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelsTotal</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 保存的图像中的像素数。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 状态</span> </p> </td> 
   <td> <p> 枚举 </p> </td> 
   <td> <p> <span class="codeph"> 如果</span> 成功了。 </p> </td> 
  </tr> 
 </tbody> 
</table>

如果请求成功，则返回HTTP响应状态200；如果请求失败或超时，则返回403。 响应的MIME类型为`text/plain`，不可缓存。

重要信息：必须通过指定`attribute::SavePath`中现有可写文件夹的路径来启用保存到文件。 `saveToFile=` 如果为空， `attribute::SavePath` 则失败。

*`file`* 是必需的，且必须是与组合的相对路径 `attribute::SavePath`。图像服务不创建文件夹。 目标文件夹必须存在于服务器上，并且具有图像服务的相应权限设置才能创建文件。

`timeout=` 为可选。默认超时为60,000毫秒，或者以`PS::SaveTimeout`配置的值为准。
