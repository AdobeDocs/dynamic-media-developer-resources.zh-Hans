---
description: 多位速率数据。
seo-description: 多位速率数据。
seo-title: mbrSet
solution: Experience Manager
title: mbrSet
topic: Scene7 Image Serving - Image Rendering API
uuid: 829c44ce-c66a-49a9-ba69-9e8e94ef8921
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# mbrSet{#mbrset}

多位速率数据。

`req=mbrSet[,text|xml[, *`编`*]][&fmt= *`码fmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 编码</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m| m3u8</span> </p></td> 
 </tr> 
</table>

返回文本或xml响应，该响应包含与与网络路径ID关联的视频集中的有效视频条目相对应的URL列表（和相应的位速率）。

先前要求有效视频条目包含值的要求现 `catalog::VideoBitRate` 已放宽。 该条目可包含或 `catalog::VideoBitRate`*或&#x200B;*`catalog::AudioBitRate`*的值*`catalog::TotalStreamBitRate`。 只需定义其中一项，视频条目即可生效。 请注意，对于有效视 `catalog::Path` 频文件扩展名的要求没有更改。

响应旨在供Apple和Flash流服务器使用，因此结构符合这些规范。 URL是使用前缀和 `attribute::HttpAppleStreamingContext` 生成 `attribute::HttpFlashStreamingContext`的。

m3u8响应仅包含视频集中存在的mp4文件。 如果没有mp4文件，则这些响应仅包含f4v文件。 如果没有mp4文件或f4v文件，则响应为空。

f4m响应仅包含视频集中存在的f4v文件。 如果没有f4v文件，则这些响应仅包含mp4文件。 如果不存在f4v文件或mp4文件，则响应为空。

f4m/m3u8响应中显示的比特率与中的值(转换为相 `catalog::TotalStreamBitRate` 应的单位)相对应。 如 `catalog::TotalStreamBitRate` 果未定义，则使用和 `catalog::VideoBitRate` 的 `catalog::AudioBitRate` 总和。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::NonImgExpiration`.
