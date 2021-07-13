---
description: 多比特率数据。
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 4%

---

# mbrSet{#mbrset}

多比特率数据。

`req=mbrSet[,text|xml[, *``*]][&fmt= *`encodingfmtType`*]`

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

返回文本或xml响应，该响应包含与与网络路径ID关联的视频集中的有效视频条目相对应的URL列表（及相应的比特率）。

以前关于有效视频条目包含`catalog::VideoBitRate`值的要求现已放宽。 该条目可以包含&#x200B;`catalog::VideoBitRate`*或* `catalog::AudioBitRate`*或* `catalog::TotalStreamBitRate`的值。 只需定义其中一项，视频条目即可生效。 请注意，`catalog::Path`和有效视频文件扩展名的要求未更改。

响应旨在供Apple和Flash流服务器使用，因此在结构上符合这些规范。 URL使用前缀`attribute::HttpAppleStreamingContext`和`attribute::HttpFlashStreamingContext`生成。

m3u8响应仅包含mp4文件（如果视频集中存在）。 如果不存在mp4文件，则这些响应仅包含f4v文件。 如果不存在mp4文件或f4v文件，则响应为空。

如果视频集中存在f4v文件，则f4m响应仅包含f4v文件。 如果不存在f4v文件，则这些响应将仅包含mp4文件。 如果不存在f4v文件或mp4文件，则响应为空。

f4m/m3u8响应中显示的比特率与`catalog::TotalStreamBitRate`中的值相对应（转换为相应的单位）。 如果未定义`catalog::TotalStreamBitRate`，则使用`catalog::VideoBitRate`和`catalog::AudioBitRate`的总和。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::NonImgExpiration`.
