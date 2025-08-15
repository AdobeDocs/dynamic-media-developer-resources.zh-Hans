---
description: 多位速率数据。
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# mbrSet{#mbrset}

多位速率数据。

`req=mbrSet[,text|xml[, *`编码`*]][&fmt= *`fmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">编码</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

返回文本或xml响应，其中包含URL（以及相应的比特率）列表，这些URL与网络路径ID关联的视频集中的有效视频条目相对应。

以前要求有效视频条目包含`catalog::VideoBitRate`值的要求现已放松。 该项可以包含&#x200B;`catalog::VideoBitRate`*或* `catalog::AudioBitRate`*或* `catalog::TotalStreamBitRate`的值。 要使视频条目有效，只需定义其中的一个即可。 请注意，`catalog::Path`和有效的视频文件扩展名的要求未发生更改。

响应旨在供Apple和Flash Streaming Server使用，因此在结构上符合这些规范。 使用前缀`attribute::HttpAppleStreamingContext`和`attribute::HttpFlashStreamingContext`生成URL。

m3u8响应仅包含mp4文件（如果视频集中存在任何文件）。 如果没有mp4文件，则这些响应仅包含f4v文件。 如果既不存在mp4文件，也不存在f4v文件，则响应为空。

f4m响应仅包含f4v文件（如果视频集中存在任何文件）。 如果不存在任何f4v文件，则这些响应仅包含mp4文件。 如果既不存在f4v文件，也不存在mp4文件，则响应为空。

显示在f4m/m3u8响应中的比特率对应于`catalog::TotalStreamBitRate`中的值（转换为适当的单位）。 如果未定义`catalog::TotalStreamBitRate`，则使用`catalog::VideoBitRate`和`catalog::AudioBitRate`的总和。

可使用基于`catalog::NonImgExpiration`的TTL来缓存HTTP响应。
