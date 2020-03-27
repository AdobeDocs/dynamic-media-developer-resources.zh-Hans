---
description: 作业类型允许授权导出以前上传的文件。
seo-description: 作业类型允许授权导出以前上传的文件。
seo-title: ExportJob
solution: Experience Manager
title: ExportJob
topic: Scene7 Image Production System API
uuid: 439e3dd8-85b8-4f5b-abf8-8cc5a3f59fe6
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ExportJob{#exportjob}

作业类型允许授权导出以前上传的文件。

ExportJob不支持以下资产类型：

* 图像集
* 渲染集
* 旋转集
* 媒体集
* 多比特率集
* 视频集
* eCatalog
* 优惠套餐

<table id="table_D8F3FD30D15648BFA5B980D3DC0A5AB1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>列表 <span class="codeph"> 需要导出的</span> assetHandle。 请参 <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> 阅HandleArray</a>。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fmt</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>指定导出的类 <span class="codeph"> 型。可能的值</span>:[原始，转换] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">如果 <span class="codeph"> fmt=orig</span>，则资源将作为原始资源导出 </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">如 <span class="codeph"> 果fmt=convert</span>，则资产将转换为is_modifer或宏输入参数中 <span class="codeph"> 指定的格式</span> , <span class="codeph"> 或</span> macro input参数 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> is_modifier</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>指定ImageServer <span class="codeph"> rendering URL字符串，该字符串将附加到ExportJob</span> convert请求中 <span class="codeph"></span> 。 </p> <p>有关发送IS修饰符 <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/" scope="external" format="html"> 的详细信息</a> ，请参阅IS文档。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 宏</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 电子 <span class="varname"> 邮件设置</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>选择电子邮件设置。 可能的值︰ </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> <span class="codeph"> 所有</span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph"> 错误</span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> ErrorAndWarning</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph"> 作业完成</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph"> 无</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 客 <span class="varname"> 户端ID</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>指定启动导出请求的客户端或客户的IP地址。 </p> <p> <p>注意： 此参数当前未填充，且仅保留为将来使用。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

对于同时提供和 `fmt=convert` 提供的 `is_modifier` ExportJob `macro` 请求，目标文件遵循由提供的格式 `macro`。 例如：

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```

