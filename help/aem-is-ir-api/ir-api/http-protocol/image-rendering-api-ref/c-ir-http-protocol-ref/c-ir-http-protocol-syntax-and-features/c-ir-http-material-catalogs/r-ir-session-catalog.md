---
title: 会话目录
description: 会话目录是材料目录，为请求提供会话属性，并为所有src=、vignette=和icc=命令提供默认catId值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# 会话目录{#session-catalog}

会话目录是材料目录，为请求提供会话属性，并为所有`src=`、`vignette=`和`icc=`命令提供默认catId值。

会话目录被指定为HTTP请求路径的第一个路径元素（紧随服务器名称之后）。 如果第一个路径元素与任何目录的attribute：：RootId不匹配，则将默认目录用作会话目录。

会话目录提供了以下会话默认值：

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>属性 </p> </th> 
   <th class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">属性：：RootPath</span> </p> </td> 
   <td> <p> 材料数据文件的根路径 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：VignettePath</span> </p> </td> 
   <td> <p> 晕影文件的根路径 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：IccProfileRgb</span> </p> </td> 
   <td> <p> 如果晕影未嵌入ICC配置文件，则默认工作色彩空间 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：RootUrl</span> </p> </td> 
   <td> <p> <span class="codeph"> src=</span>命令中相对HTTP文件路径的根URL </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：ShowOverlapObjs</span> </p> </td> 
   <td> <p> 重叠对象的初始显示/隐藏状态 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：Expiration</span> </p> </td> 
   <td> <p> 代理服务器和浏览器缓存的回复图像的生存时间值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：MaxPix</span> </p> </td> 
   <td> <p> 允许的最大回复图像宽度和高度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：DefaultPix</span> </p> </td> 
   <td> <p> <span class="codeph"> wid=</span>和<span class="codeph"> hei=</span>的默认值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：Format</span> </p> </td> 
   <td> <p> <span class="codeph"> fmt=</span>的默认值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：JpegQuality</span> </p> </td> 
   <td> <p> <span class="codeph"> qlt=</span>的默认值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：TiffEncoding</span> </p> </td> 
   <td> <p> 用于TIFF图像输出的压缩类型 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：锐化</span> </p> </td> 
   <td> <p> <span class="codeph">锐化的默认值=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：OnFailSel</span> </p> </td> 
   <td> <p> 指定<span class="codeph"> sel=</span>命令失败时的行为 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：OnFailObj</span> </p> </td> 
   <td> <p> 指定<span class="codeph"> obj=</span>命令失败时的行为 </p> </td> 
  </tr> 
 </tbody> 
</table>
