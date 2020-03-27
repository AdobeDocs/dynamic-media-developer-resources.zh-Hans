---
description: 帮助您定义搜索条件以提高搜索效率的过滤器。
seo-description: 帮助您定义搜索条件以提高搜索效率的过滤器。
seo-title: SearchFilter
solution: Experience Manager
title: SearchFilter
topic: Scene7 Image Production System API
uuid: 85a434d3-51a5-4e68-901e-70585c0e8b20
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SearchFilter{#searchfilter}

帮助您定义搜索条件以提高搜索效率的过滤器。

语法

## 参数 {#section-4c611d9bbe0d418d882632605fc4d29d}

<table id="table_57CEE262A33A4E898C6AFB30C93FD874"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 文 <span class="varname"> 件夹</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 指定要搜索的文件夹。 留空可搜索整个公司。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 包含子 <span class="varname"> 文件夹</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">设置为： 
    <ul id="ul_BD8686943BD14D05A21C00192D4D70D3"> 
     <li id="li_B6A6DE5AAEFF4A80A8413B4785A88222"><span class="codeph"> 真的</span>:搜索已命名的文件夹和所有子文件夹。 </li> 
     <li id="li_10A581F98B4847ED8EBE4AECC3AD70A8"><span class="codeph"> 错误</span>:仅搜索已命名的文件夹。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">要在搜索中返回的资产类型列表。 例如，图 <span class="codeph"> 像</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3"> 指定要从搜索中排除的资产类型。 例如，图像。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">列表要在搜索中返回的资产子类型。 例如，对于 <span class="codeph"> Asset</span>，您可以搜索 <span class="codeph"> MediaType</span> 子类型。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> strictSubTypeCheck</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>一个可选的布尔标志，它指定在传递assetSubTypeArray时是否返回 <span class="codeph"> 无子类型的资产</span> 。 </p> <p>如果为true，则只返回具有某个指定子类型的资产。 </p> <p>如果为false，则不返回子类型的资产。 </p> <p>默认值为false。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 排 <span class="varname"> 除副产品</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">设置为： 
    <ul id="ul_8C164A5D9F0F43968C86A67FA6884F35"> 
     <li id="li_D8009688FF2C439D98D6C1052C1A6CBE"><span class="codeph"> 真的</span>:仅返回原始资产。 </li> 
     <li id="li_4970226BF0FF42388CAE4415FB63AF16"><span class="codeph"> 错误</span>:返回生成的内容。 例如，来自已上载PDF的图像。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 项 <span class="varname"> 目处理</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 处理要搜索的项目。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">指定: 
    <ul id="ul_96FFEE28F7624C1FB0356776B4C7CD53"> 
     <li id="li_DCB07288E5F44E05A4D83D3F34B0E08E"><span class="codeph"> MarkedForPublish</span> ，仅返回已发布的资产。 </li> 
     <li id="li_9A9A852248DB490DB958AE986DF02672"><span class="codeph"> NotMarkedForPublish</span> ，仅返回未发布的资产。 </li> 
    </ul> <p>注意：留空可搜索所有已发 <i>布状态</i> 类型。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 垃圾 <span class="varname"> 状态</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">指定: 
    <ul id="ul_D31B903FA8DA4CFFABAFABA3D8DA91EC"> 
     <li id="li_E4386C8260E64F0BAFE5BA57FF788E48"><span class="codeph"> 返回资产</span> （无论其垃圾桶状态如何）的任意选项。 </li> 
     <li id="li_0B8933FE18C643828075EC8CE8C0223C"><span class="codeph"> NotInTrash</span> 将返回“正常”资源。 </li> 
     <li id="li_A1F46A0762FA4D4BA9F7247338238DC6"><span class="codeph"> InTrash</span> ，以从垃圾桶返回资源。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

