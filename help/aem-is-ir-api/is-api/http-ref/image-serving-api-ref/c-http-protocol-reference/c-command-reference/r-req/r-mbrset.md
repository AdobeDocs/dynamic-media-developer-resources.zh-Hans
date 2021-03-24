---
description: 多位速率数据。
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '267'
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

返回文本或xml响应，该响应包含URL列表（和相应的位速率），这些URL对应于与网络路径ID关联的视频集中的有效视频条目。

以前关于有效视频条目包含`catalog::VideoBitRate`值的要求现已放宽。 该条目可包含&#x200B;`catalog::VideoBitRate`*或* `catalog::AudioBitRate`*或* `catalog::TotalStreamBitRate`的值。 只需定义其中一个，视频条目即可生效。 请注意，`catalog::Path`和有效视频文件扩展名的要求没有更改。

响应旨在供Apple和Flash Streaming Server使用，因此结构符合这些规范。 使用前缀`attribute::HttpAppleStreamingContext`和`attribute::HttpFlashStreamingContext`生成URL。

m3u8响应仅包含mp4文件（如果视频集中存在任何文件）。 如果没有mp4文件，则这些响应仅包含f4v文件。 如果没有mp4文件或f4v文件，则响应为空。

f4m响应仅包含视频集中存在的f4v文件。 如果没有f4v文件，则这些响应仅包含mp4文件。 如果没有f4v文件或mp4文件，则响应为空。

f4m/m3u8响应中显示的比特率与`catalog::TotalStreamBitRate`（转换为相应单位）中的值相对应。 如果未定义`catalog::TotalStreamBitRate`，则使用`catalog::VideoBitRate`和`catalog::AudioBitRate`的和。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::NonImgExpiration`.
