---
description: 播放日志实用程序可用于预生成HTTP响应缓存的内容。
solution: Experience Manager
title: “playlog”实用程序
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0213978-3a1d-44b4-82bf-4527b980b29e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# “playlog”实用程序{#the-playlog-utility}

播放日志实用程序可用于预生成HTTP响应缓存的内容。

在主要版本升级后（当版本号的第一位或第二位发生更改时），现有的图像服务HTTP响应缓存无法保证可用。 如果升级后服务器要处于满载状态，则服务器可能会过载并处理最初几小时的缓存未命中请求，直到合理填充缓存且缓存命中率增加为止。

为避免此初始负载尖峰，`playlog`实用程序可用于预生成HTTP响应缓存的内容。 `playlog`从现有的访问日志文件提取HTTP请求并将其发送到服务器以生成缓存项。 对于典型使用情形，播放包含一整天流量的单个访问日志文件就足够了。

除了在升级安装后预置HTTP响应缓存之外，该实用程序还用于在向负载平衡环境添加新服务器时预生成缓存内容；只需从其他服务器之一回放最近的日志文件即可。

可以将`playlog`配置为支持由早期版本的图像服务生成的大多数访问日志文件。

## 使用 {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p <span class="varname">前缀</span> </span> </p> </td> 
  <td class="stentry"> <p>根URL，附加到从日志文件提取的请求之前。 </p> <p>默认： <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n <span class="varname">列</span> </span> </p> </td> 
  <td class="stentry"> <p>日志记录中包含请求的字段（列）编号；从1开始。 </p> <p>默认值：16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s <span class="varname">分隔符</span> </span> </p> </td> 
  <td class="stentry"> <p>字段分隔符；正则表达式模式。 </p> <p>默认： <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m <span class="varname">标记</span> </span> </p> </td> 
  <td class="stentry"> <p>请求标记；标识日志文件中应播放的请求；正则表达式模式。 </p> <p>默认：<span class="codeph">请求：</span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x <span class="varname">后缀</span> </span> </p> </td> 
  <td class="stentry"> <p>附加到从日志文件提取的请求的后缀；可用于将播放的请求与日志文件中的实时请求分开；“？” 或自动插入“&amp;”分隔符；后缀可以按大括号内的位置引用任何日志字段，默认值对应于md5签名字段。 </p> <p>默认： <span class="codeph">播放日志={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>详细模式，将生成的请求URL打印到<span class="codeph"> stdout </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h </span> </p> </td> 
  <td class="stentry"> <p>将摘要打印到<span class="codeph"> stdout </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method — 要使用的HTTP请求方法(<span class="codeph"> get|post|head|smart </span>)。 </p> <p>默认：<span class="codeph">智能</span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos — 日志文件中的pos，从中获取原始方法。 </p> <p>默认值：15 </p> </td> 
 </tr> 
</table>

对于Windows，文件名为[!DNL playlog.bat]，在Linux上为[!DNL playlog.sh]。

## 示例 {#section-716e5c35e9fa4ee3a4b0687381fcea40}

以下示例回放图像服务在Linux上创建的访问日志文件中的所有请求：

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

以下命令将回放在Windows上的映像服务创建的跟踪日志文件中找到的所有请求：

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
