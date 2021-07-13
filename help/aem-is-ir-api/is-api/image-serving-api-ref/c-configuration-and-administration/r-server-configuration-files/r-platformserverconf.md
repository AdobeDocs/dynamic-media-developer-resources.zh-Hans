---
description: 包含Platform Server设置。
solution: Experience Manager
title: PlatformServer.conf
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,User
exl-id: 00d55453-e7e6-4242-be83-7efa12764e5d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%

---

# PlatformServer.conf{#platformserver-conf}

包含Platform Server设置。

此文件是JAVA属性文件。 必须注意遵守适当的公约；否则，平台服务器可能无法启动。 在Windows文件路径中，使用双反斜杠“\\”或单正斜杠“/”，而不是反斜杠“\”。 在此类型的文件中，反斜线用作转义字符。

对此文件所做的更改将在保存文件后生效。

[!DNL PlatformServer.conf]中只能更改下面列出的设置。 如果缺少特定设置，则可以在文件中的任意位置添加该设置。 每个设置只能有一个实例。

<table id="simpletable_38244750F50A46E5B0077F5F860B125C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>常规平台服务器设置 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cache.rootPaths=./cache </span> </p> <p> <span class="codeph"> cache.maxEntries=1000000  </span> </p> <p> <span class="codeph"> cache.maxSize=1073741824  </span> </p> <p> <span class="codeph"> isConnection.port=27345  </span> </p> <p> <span class="codeph"> allowDefaultCatalogRequests=true  </span> </p> <p> <span class="codeph"> saveToFile.saveTimeout=60000  </span> </p> <p> <span class="codeph"> staticContent.rootPaths=./static-content </span> </p> </td> 
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
  <td class="stentry"> <p> <span class="codeph"> svgProvider.rootPaths=./图像 </span> </p> <p> <span class="codeph"> svgProvider.SVGFileSizeLimit=1024  </span> </p> <p> <span class="codeph"> svgProvider.port=8080  </span> </p> <p> <span class="codeph"> svgProvider.fontRoot=./图像 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>媒体集响应 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fvctx.useCatalogRecordValidation=false  </span> </p> <p> <span class="codeph"> fvctx.nestingLimit=10  </span> </p> <p> <span class="codeph"> fvctx.brochureLimit=20  </span> </p> </td> 
 </tr> 
</table>
