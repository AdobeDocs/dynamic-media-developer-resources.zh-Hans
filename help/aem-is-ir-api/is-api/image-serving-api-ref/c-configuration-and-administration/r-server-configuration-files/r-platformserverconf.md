---
description: 包含平台服务器设置。
seo-description: 包含平台服务器设置。
seo-title: PlatformServer.conf
solution: Experience Manager
title: PlatformServer.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: d798762b-c9ff-4e1b-b2ac-c5e40476b375
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%

---


# PlatformServer.conf{#platformserver-conf}

包含平台服务器设置。

此文件是JAVA属性文件。 必须注意遵守适当的公约；否则，平台服务器可能无法开始。 在Windows文件路径中，使用多次反斜杠“\\”或单个正斜杠“/”，而不是反斜杠“\”。 反斜杠在此类型的文件中用作转义字符。

对此文件所做的更改将在保存文件后生效。

[!DNL PlatformServer.conf]中只能更改下面列出的设置。 如果某个特定设置不存在，则可在文件的任意位置添加该设置。 每个设置只能有一个实例。

<table id="simpletable_38244750F50A46E5B0077F5F860B125C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>一般平台服务器设置 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cache.rootPaths=。/cache </span> </p> <p> <span class="codeph"> cache.maxEntries=1000000  </span> </p> <p> <span class="codeph"> cache.maxSize=1073741824  </span> </p> <p> <span class="codeph"> isConnection.port=27345  </span> </p> <p> <span class="codeph"> allowDefaultCatalogRequests=true  </span> </p> <p> <span class="codeph"> saveToFile.saveTimeout=60000  </span> </p> <p> <span class="codeph"> staticContent.rootPaths=。/static内容</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>缓存群集配置 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cluster.hosts=&lt;empty&gt; </span> </p> <p> <span class="codeph"> cacheCluster.queryTimeout=50  </span> </p> <p> <span class="codeph"> cacheCluster.fetchTimeout=10000  </span> </p> <p> <span class="codeph"> cacheCluster.updateLocalCache=true  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>重定向配置时出错 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> errorRedirect.rootUrl=&lt;empty&gt; </span> </p> <p> <span class="codeph"> errorRedirect.connectTimeout=1000  </span> </p> <p> <span class="codeph"> errorRedirect.socketTimeout=30000  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>SVG配置 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> svgProvider.rootPaths=。/图像 </span> </p> <p> <span class="codeph"> svgProvider.SVGFileSizeLimit=1024  </span> </p> <p> <span class="codeph"> svgProvider.port=8080  </span> </p> <p> <span class="codeph"> svgProvider.fontRoot=。/图像 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>媒体集响应 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fvctx.useCatalogRecordValidation=false  </span> </p> <p> <span class="codeph"> fvctx.nestingLimit=10  </span> </p> <p> <span class="codeph"> fvctx.brochureLimit=20  </span> </p> </td> 
 </tr> 
</table>

