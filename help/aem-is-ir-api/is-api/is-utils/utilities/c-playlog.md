---
description: 播放日志实用程序可用于预生成HTTP响应缓存的内容。
solution: Experience Manager
title: “playlog”实用程序
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: e0213978-3a1d-44b4-82bf-4527b980b29e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 1%

---

# “playlog”实用程序{#the-playlog-utility}

播放日志实用程序可用于预生成HTTP响应缓存的内容。

在主版本升级后（当版本号的第一位或第二位发生更改时），无法保证现有的图像服务HTTP响应缓存可用。 如果服务器在升级后要处于全负载状态，则服务器可能会在处理缓存未命中请求的前几个小时进行重载，直到缓存被合理填充并且缓存命中率增加为止。

为避免此初始加载尖峰，可使用`playlog`实用程序预生成HTTP响应缓存的内容。 `playlog` 从现有访问日志文件中提取HTTP请求，并将其发送到服务器以生成缓存条目。对于典型的使用情况，只需播放包含一整天流量的单个访问日志文件即可。

除了在升级安装后启动HTTP响应缓存外，该实用程序还用于在向负载平衡环境添加新服务器时预生成缓存内容；只需从其他服务器之一播放最近的日志文件即可。

`playlog` 可以配置为支持由以前版本的图像服务生成的大多数访问日志文件。

## 使用 {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p前 <span class="varname"> 缀  </span> </span> </p> </td> 
  <td class="stentry"> <p>根URL，用于将从日志文件提取的请求附加到前面。 </p> <p>默认：<span class="filepath"> http://localhost:8080/is </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n <span class="varname"> 列  </span> </span> </p> </td> 
  <td class="stentry"> <p>字段（列）编号，其中包含日志记录中的请求；基于1。 </p> <p>默认：16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s分 <span class="varname"> 隔符  </span> </span> </p> </td> 
  <td class="stentry"> <p>字段分隔符；正则表达式模式。 </p> <p>默认: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m标 <span class="varname"> 记  </span> </span> </p> </td> 
  <td class="stentry"> <p>请求标记；标识日志文件中应播放的请求；正则表达式模式。 </p> <p>默认：<span class="codeph">请求：</span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x后 <span class="varname"> 缀  </span> </span> </p> </td> 
  <td class="stentry"> <p>附加在从日志文件提取的请求中的后缀；可用于将播放请求与日志文件中的实时请求分开；a '?' 或自动插入“&amp;”分隔符；后缀可以按大括号内的位置引用任何日志字段，默认值与md5签名字段相对应。 </p> <p>默认：<span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>详细模式下，将生成的请求URL打印到<span class="codeph"> stdout </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h </span> </p> </td> 
  <td class="stentry"> <p>将总结内容打印到<span class="codeph"> stdout </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method — 要使用的HTTP请求方法(<span class="codeph"> get|post|head|smart </span>)。 </p> <p>默认：<span class="codeph">智能</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos — 日志文件中用于从中获取原始方法的pos。 </p> <p>默认：15 </p> </td> 
 </tr> 
</table>

对于Windows，文件名为[!DNL playlog.bat]，在Linux上为[!DNL playlog.sh]。

## 示例 {#section-716e5c35e9fa4ee3a4b0687381fcea40}

以下示例回放由Linux上的图像服务创建的访问日志文件中的所有请求：

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

以下命令将播放在Windows上的图像服务创建的跟踪日志文件中找到的所有请求：

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
