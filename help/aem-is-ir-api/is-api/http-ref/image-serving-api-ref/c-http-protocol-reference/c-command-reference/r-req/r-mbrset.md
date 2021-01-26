---
description: 多位速率数据。
seo-description: 多位速率数据。
seo-title: mbrSet
solution: Experience Manager
title: mbrSet
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 829c44ce-c66a-49a9-ba69-9e8e94ef8921
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 4%

---


# mbrSet{#mbrset}

多位速率数据。

`req=mbrSet[,text|xml[, *`编`*]][&fmt= *`码fmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 编码</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

返回文本或xml响应，该响应包含与网络路径ID关联的视频集中的有效视频条目相对应的URL列表（和相应的比特率）。

以前要求有效视频条目包含`catalog::VideoBitRate`值的要求现已放宽。 该条目可包含&#x200B;`catalog::VideoBitRate`*或* `catalog::AudioBitRate`*或* `catalog::TotalStreamBitRate`的值。 只需定义其中一项，视频条目即可生效。 请注意，`catalog::Path`和有效视频文件扩展名的要求没有更改。

响应旨在供Apple和Flash流服务器使用，因此结构上符合这些规范。 URL是使用前缀`attribute::HttpAppleStreamingContext`和`attribute::HttpFlashStreamingContext`生成的。

m3u8响应仅包含视频集中存在的mp4文件（如果存在）。 如果没有mp4文件，则这些响应仅包含f4v文件。 如果没有mp4文件或f4v文件，则响应为空。

f4m响应仅包含视频集中存在的f4v文件。 如果没有f4v文件，则这些响应仅包含mp4文件。 如果不存在f4v文件和mp4文件，则响应为空。

f4m/m3u8响应中显示的比特率与`catalog::TotalStreamBitRate`（转换为相应的单位）中的值相对应。 如果未定义`catalog::TotalStreamBitRate`，则使用`catalog::VideoBitRate`和`catalog::AudioBitRate`的和。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::NonImgExpiration`.
