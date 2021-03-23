---
description: playlog实用程序可用于预生成HTTP响应缓存的内容。
seo-description: playlog实用程序可用于预生成HTTP响应缓存的内容。
seo-title: “playlog”实用程序
solution: Experience Manager
title: “playlog”实用程序
uuid: 9044515e-7cfb-4e86-9ac4-e071b60f38d1
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 1%

---


# “playlog”实用程序{#the-playlog-utility}

playlog实用程序可用于预生成HTTP响应缓存的内容。

现有的图像服务HTTP响应缓存在主版本升级后（当版本号的第一位或第二位更改时）无法保证可用。 如果服务器在升级后要处于全负载状态，则服务器可能会在处理高速缓存未命中请求的前几个小时之前过载，直到合理填充高速缓存并且高速缓存命中率增加。

为避免此初始加载尖峰，`playlog`实用程序可用于预生成HTTP响应缓存的内容。 `playlog` 从现有访问日志文件中提取HTTP请求，并将其发送到服务器以生成缓存条目。对于典型的使用情况，只需播放包含全天流量的单个访问日志文件即可。

除了在升级安装后启动HTTP响应缓存外，在将新服务器添加到负载平衡环境时，该实用程序还用于预生成缓存内容；只需从其他服务器中播放最近的日志文件即可。

`playlog` 可以配置为支持由先前版本的图像服务生成的大多数访问日志文件。

## 使用 {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p前 <span class="varname"> 缀  </span> </span> </p> </td> 
  <td class="stentry"> <p>根URL，在从日志文件提取的请求前面添加。 </p> <p>默认：<span class="filepath"> http://localhost:8080/is </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n <span class="varname"> 列  </span> </span> </p> </td> 
  <td class="stentry"> <p>字段（列）编号，在日志记录中包含请求；基于1。 </p> <p>默认：16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s分 <span class="varname"> 隔符  </span> </span> </p> </td> 
  <td class="stentry"> <p>字段分隔符；常规表达式模式。 </p> <p>默认: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m标 <span class="varname"> 记  </span> </span> </p> </td> 
  <td class="stentry"> <p>请求标记；标识日志文件中应播放的请求；常规表达式模式。 </p> <p>默认：<span class="codeph">请求：</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x后 <span class="varname"> 缀  </span> </span> </p> </td> 
  <td class="stentry"> <p>在从日志文件提取的请求后附加后缀；可用于将播放的请求与日志文件中的实时请求分开；“？” 或"&amp;"分隔符自动插入；后缀可以按花括号中的位置引用任何日志字段，默认值与md5签名字段相对应。 </p> <p>默认：<span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>详细模式，将生成的请求URL打印到<span class="codeph"> stdout </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h </span> </p> </td> 
  <td class="stentry"> <p>将总结打印到<span class="codeph"> stdout </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method — 要使用的HTTP请求方法(<span class="codeph"> get|post|head|smart </span>)。 </p> <p>默认：<span class="codeph"> smart </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos — 日志文件中用于从中获取原始方法的pos。 </p> <p>默认：15 </p> </td> 
 </tr> 
</table>

对于Windows，文件名为[!DNL playlog.bat]，在Linux中为[!DNL playlog.sh]。

## 示例 {#section-716e5c35e9fa4ee3a4b0687381fcea40}

以下示例播放由Linux上的图像服务创建的访问日志文件中的所有请求：

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

以下命令将播放在Windows上的图像服务创建的跟踪日志文件中找到的所有请求：

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
