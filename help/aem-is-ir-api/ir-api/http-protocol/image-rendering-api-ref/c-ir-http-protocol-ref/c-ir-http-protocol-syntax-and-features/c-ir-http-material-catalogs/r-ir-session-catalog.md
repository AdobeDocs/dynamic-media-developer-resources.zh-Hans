---
description: 会话目录是提供请求的会话属性以及所有src=、vignette=和icc=命令的默认catId值的材料目录。
seo-description: 会话目录是提供请求的会话属性以及所有src=、vignette=和icc=命令的默认catId值的材料目录。
seo-title: 会话目录
solution: Experience Manager
title: 会话目录
topic: Scene7 Image Serving - Image Rendering API
uuid: 69c0f6cd-dfaf-47bf-bdd9-7abb4e6f7465
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 会话目录{#session-catalog}

会话目录是提供请求的会话属性以及所有src=、vignette=和icc=命令的默认catId值的材料目录。

会话目录指定为HTTP请求路径的第一个路径元素（紧接在服务器名后）。 如果第一个路径元素与任何目录的属性：:RootId不匹配，则默认目录将用作会话目录。

会话目录提供以下会话默认值：

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>属性 </p> </th> 
   <th class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> 材料数据文件的根路径 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:VignettePath</span> </p> </td> 
   <td> <p> 晕影文件的根路径 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:IccProfileRgb</span> </p> </td> 
   <td> <p> 如果暗角未嵌入ICC用户档案，则默认工作色彩空间 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:RootUrl</span> </p> </td> 
   <td> <p> src=命令中相对HTTP文件路径的 <span class="codeph"> 根URL</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:ShowOverlapObjs</span> </p> </td> 
   <td> <p> 重叠对象的初始显示／隐藏状态 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:Expiration</span> </p> </td> 
   <td> <p> 代理服务器和浏览器缓存的回复图像的实时时间值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:MaxPix</span> </p> </td> 
   <td> <p> 允许的最大回复图像宽度和高度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:DefaultPix</span> </p> </td> 
   <td> <p> wid=和 <span class="codeph"> hei=的</span><span class="codeph"> 默认值</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：：格式</span> </p> </td> 
   <td> <p> fmt=的默 <span class="codeph"> 认值</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:JpegQuality</span> </p> </td> 
   <td> <p> qlt=的默 <span class="codeph"> 认值</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:TiffEncoding</span> </p> </td> 
   <td> <p> TIFF图像输出的压缩类型 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：：锐化</span> </p> </td> 
   <td> <p> 锐化的默 <span class="codeph"> 认值=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:OnFailSel</span> </p> </td> 
   <td> <p> 指定sel=命令失 <span class="codeph"> 败时的行</span> 为 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:OnFailObj</span> </p> </td> 
   <td> <p> 指定obj=命令失 <span class="codeph"> 败时的行</span> 为 </p> </td> 
  </tr> 
 </tbody> 
</table>

