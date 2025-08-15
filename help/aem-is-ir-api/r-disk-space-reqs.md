---
title: 磁盘空间要求和建议
description: 除了安装软件所需的空间之外，“映像服务”还具有以下磁盘空间要求。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# 磁盘空间要求和建议{#disk-space-requirements-and-recommendations}

除了安装软件所需的空间之外，映像服务还具有以下磁盘空间要求：

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>描述/默认位置/设置方式</b> </th> 
   <th class="entry"> <b>计算/推荐</b> </th> 
   <th class="entry"> <b>个评论</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Source图像、字体、ICC配置文件</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/映像</span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS：：RootPaths </span> </p> </td> 
   <td> <p>各不相同；请参阅下面的注释。 </p> </td> 
   <td> <p>只能供图像服务器访问；服务器从不修改数据。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP响应数据缓存</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS：：ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer：：cache.maxSize </span> x 2；建议至少为2 GB。 </p> </td> 
   <td> <p>此缓存还存储嵌套/嵌入的数据和外部源图像。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>图像目录数据缓存</b> </p> <p> <span class="filepath"> <span class="varname">安装文件夹</span>/缓存/目录</span> </p> <p> <span class="codeph"> CS：：CatalogCacheFolder </span> </p> </td> 
   <td> <p>允许目录文件夹使用空间的1.5倍。 </p> </td> 
   <td> <p>最初加载目录时填充。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>记录数据</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/日志</span> </p> <p> <span class="codeph"> PS：：LogFolder </span> </p> <p> <span class="codeph"> IS：：LogFile </span> </p> <p> <span class="codeph"> SV：：LogFile </span> </p> </td> 
   <td> <p>100 MB或更多。 </p> </td> 
   <td> <p>该值因日志记录配置和服务器使用而异。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>映像服务器临时文件</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph"> IS：：TempDirectory </span> </p> <p> <span class="codeph"> SV：：TempDirectory </span> </p> </td> 
   <td> <p>100 MB足以满足大多数使用要求。 </p> </td> 
   <td> <p>短期数据；对于PTIFF以外的源图像和某些响应图像格式可能需要。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 源映像的磁盘空间要求 {#section-317da75099ad480d9a461c7e706d4f1c}

Adobe建议使用图像转换器命令行工具(IC)将所有源图像转换为金字塔TIFF文件格式(PTIFF)。 此转换确保所有应用程序的图像服务都具有最佳运行时性能。 虽然图像服务器可以处理IC接受的所有源文件格式，但Dynamic Media不支持此类使用。

使用PTIFF文件时，以下经验规则可帮助您确定空间要求。

*`total_space`* （字节） = *`number_of_images`* × (2000 + *`avg_pixel_count`* x *`avg_num_components`* × *`p_factor`*)

* *`avg_pixel_count`*&#x200B;所有原始源图像的平均像素大小（宽度x高度）。 例如，如果原始图像通常在2,000像素×2,000像素左右，则为4,000,000像素。
* *`avg_num_components`*&#x200B;取决于图像的类型。 对于大多数RGB图像，其值为3；对于大多数CMYK或RGBA图像，其值为4。 如果一半图像是RGB，另一半是RGBA，请使用3.5。
* *`p_factor`*&#x200B;取决于使用IC转换图像时设置的压缩类型和质量。

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>PTIFF压缩</b> </th> 
   <th class="entry"> <b><i>p_factor</i></b> </th> 
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
   <td> <p> 1(JPEG质量95的典型值) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此近似值不考虑文件系统开销。 磁盘上的实际空间可以大很多。

**示例**

图像服务部署预计使用30,000个低分辨率的旧图像，平均大小为500 × 500 RGB像素。 新的打印质量图像数据每年增加10,000份。 典型的CMYK图像大小为4 × 6 k字节。 所有数据都经过JPEG高质量压缩。 使用三年后的磁盘空间总量估计如下：

*`total_space`* = 30,000 × (2k + 0.5k × 0.5k × 3 × 0.1) + 3 × 10,000 × (2k + 4k × 6k × 4 × 0.1) = 2.2 G + 268 GB =约270 GB

为了保证最佳质量，可以采用zip等压缩。 假设&#x200B;*`p_factor`*&#x200B;为0.4，则所需总磁盘空间量大约是四倍。 在本例中，略多于1 TB。
