---
description: '除了安装软件所需的空间之外，映像服务还有以下磁盘空间要求 '
solution: Experience Manager
title: 磁盘空间要求和建议
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 0%

---


# 磁盘空间要求和建议{#disk-space-requirements-and-recommendations}

除了安装软件所需的空间之外，映像服务还有以下磁盘空间要求：

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>说明／默认位置／设置</b> </th> 
   <th class="entry"> <b>计算／推荐</b> </th> 
   <th class="entry"> <b>注释</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>源图像、字体、ICC用户档案</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images  </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths  </span> </p> </td> 
   <td> <p>不同；请参阅以下评论。 </p> </td> 
   <td> <p>仅需要图像服务器访问；服务器永远不会修改数据。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP响应数据缓存</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is_response  </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders  </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize  </span> x 2;推荐至少2 GB。 </p> </td> 
   <td> <p>此缓存还存储嵌套／嵌入的数据和外源图像。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>图像目录数据缓存</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog  </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder  </span> </p> </td> 
   <td> <p>允许目录文件夹使用1.5倍的空间。 </p> </td> 
   <td> <p>最初载入目录时填充。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>日志数据</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs  </span> </p> <p> <span class="codeph"> PS::LogFolder  </span> </p> <p> <span class="codeph"> IS::LogFile  </span> </p> <p> <span class="codeph"> SV::LogFile  </span> </p> </td> 
   <td> <p>100 MB或更多。 </p> </td> 
   <td> <p>根据日志记录配置和服务器使用情况不同。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>图像服务器临时文件</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp  </span> </p> <p> <span class="codeph"> IS::TempDirectory  </span> </p> <p> <span class="codeph"> SV::TempDirectory  </span> </p> </td> 
   <td> <p>100 MB的US足够。 </p> </td> 
   <td> <p>短期数据；源图像可能需要PTIFF和某些响应图像格式以外的源图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 源映像{#section-317da75099ad480d9a461c7e706d4f1c}的磁盘空间要求

建议使用图像转换器命令行工具(IC)将所有源图像转换为金字塔TIFF文件格式(PTIFF)。 此转换可确保所有应用程序的图像服务的最佳运行时性能。 虽然图像服务器可以处理IC接受的所有源文件格式，但Dynamic Media不提供此类用途的支持。

使用PTIFF文件时，以下经验法则可以帮助您确定空间要求。

*`total_space`* （字节）=  *`number_of_images`* x(2000 +  *`avg_pixel_count`* x  *`avg_num_components`* x  *`p_factor`* x)

* *`avg_pixel_count`* 所有原始图像的平均像素大小（宽x高）。例如，如果原始图像通常约为2k x 2k像素，则此值为4M像素。
* *`avg_num_components`* 取决于图像的类型。对于大多数RGB图像，它为3，对于大多数CMYK或RGBA图像，它为4。 如果一半图像为RGB，另一半为RGBA，则使用3.5。
* *`p_factor`* 取决于在使用IC转换图像时设置的压缩类型和质量。

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>PTIFF压缩</b> </th> 
   <th class="entry"> <b><i>p因子</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>未压缩 </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Deflate-Compression </p> </td> 
   <td> <p> 25-0.75，具体取决于图像 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG压缩 </p> </td> 
   <td> <p> 1（JPEG质量为95的典型值） </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此近似不考虑文件系统开销。 磁盘上的实际空间可以大得多。

**示例**

图像服务部署预计使用30,000个低分辨率传统图像，平均大小为500x500 RGB像素。 新的打印质量图像数据预计将以每年10,000的速度添加。 典型CMYK图像大小将为4k x 6k字节。 所有数据都将以高质量进行JPEG压缩。 3年使用后磁盘空间总量估计如下：

*`total_space`* = 30,000 x(2k + 0.5k x 0.5k x 3 x 0.1)+ 3 x 10,000 x(2k + 4k x 4 x 0.1)= 2.2 G + 268 GB =约270 GB

为获得最佳质量，可采用deflate(zip)压缩。 假定&#x200B;*`p_factor`*&#x200B;为0.4，则所需磁盘空间总量大约是4倍。 在这个例子中，略多于1 TB。
