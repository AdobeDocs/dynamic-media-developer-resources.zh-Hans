---
description: 使用这些服务器设置进行日志记录访问。
solution: Experience Manager
title: 访问日志记录
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e677a617-115d-4f6e-9eb5-bdc14ad7ff24
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# 访问日志记录{#access-logging}

使用这些服务器设置进行日志记录访问。

语法

## TC：：directory — 日志文件文件夹 {#section-5d9e2168d4504bbe9868b7d6051c9d67}

[!DNL Platform Server]写入日志文件的文件夹。 这可以是绝对路径或相对于&#x200B;*`install_folder`*&#x200B;的路径。 默认值为&#x200B;[!DNL  *`install_folder`*/日志]。

>[!NOTE]
>
>在更改此设置之前，必须创建新文件夹。 如果安装映像服务后以非root用户帐户运行，请确保文件夹具有正确的读/写访问权限。

## TC：：maxDays — 保留日志文件的天数 {#section-45cbecffc5694c87b7d5c176a44a4885}

日志文件应保留的天数。 每天的午夜创建新日志文件。 此时，服务器将删除日志文件文件夹中所有超过指定天数的文件，包括由图像服务器或渲染服务器写入的文件。 默认值为 10。

## TC：：prefix — 访问日志文件名 {#section-1003856323b844049632710a5a056aa7}

将访问日志数据写入其中的文件的名称前缀。 日期和文件后缀([!DNL  *`yyyy`*-*`mm`*-*`dd`*.log])附加到指定的字符串。 访问日志文件的名称必须与跟踪日志文件的名称不同。 默认值为“`access-`”。

## TC：：pattern — 访问日志模式 {#section-22775ea85cee444d8a7d7336a3b1feef}

指定[!DNL Platform Server]访问日志记录的数据模式。 模式字符串指定用相应值替换的变量。 模式字符串中的所有其他字符按字面顺序传输到日志记录。

要使用缓存预热实用程序，必须将空格用作字段分隔符。 [!DNL Platform Server]将字段值中的所有空格和“%”字符分别替换为`%20`和`%25`。

支持以下模式变量：

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>模式</b> </th> 
   <th class="entry"> <b>描述</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> %a </span> </p> </td> 
   <td> <p>远程IP地址。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %A </span> </p> </td> 
   <td> <p>本地IP地址。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %b </span> </p> </td> 
   <td> <p>响应字节计数（不包括HTTP标头），或者如果为零，则为“ ”。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>不包括HTTP标头的响应字节计数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>请求处理时间（以毫秒为单位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>线程id（用于交叉引用调试/错误日志条目）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>日期和时间，格式为<span class="codeph"> <span class="varname"> yyyy </span>- <span class="varname"> MM </span>- <span class="varname"> dd </span> <span class="varname"> HH </span>： <span class="varname"> mm </span>： <span class="varname"> ss </span>。 <span class="varname"> SSS </span>偏移</span> </p> <p> （<span class="varname"> SSS </span>为毫秒，<span class="varname">偏移量</span>为GMT时间偏移量）；在将响应发送到客户端时捕获时间值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>请求方法(<span class="codeph"> GET </span>、<span class="codeph"> POST </span>等)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>请求重叠（同时处理的请求数）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>收到此请求的本地端口。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>查询字符串（以“？”为前缀） （如果存在）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>请求的第一行（请求方法、URI、HTTP版本）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p>与<span class="codeph"> %r </span>相同，但对URI应用有限的HTTP编码以避免日志分析问题。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>HTTP响应状态代码。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %S </span> </p> </td> 
   <td> <p>用户会话ID </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>日期和时间（通用日志格式）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>已进行身份验证的远程用户（如果有），否则''。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U </span> </p> </td> 
   <td> <p>URI路径。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v </span> </p> </td> 
   <td> <p>本地服务器名称。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T </span> </p> </td> 
   <td> <p>请求处理时间（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] 缓存键（缓存文件文件夹/名称）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] 缓存管理关键字： <span class="codeph"> {已重用 | 已创建 | 已更新 | 远程 | REMOTE_CREATED | 远程更新 | 远程缓存 | 已验证 | 已忽略 | 未定义} </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r </span> </p> </td> 
   <td> <p>响应MIME类型。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>发生上下文转发时的目标上下文。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r </span> </p> </td> 
   <td> <p><span class="codeph"> etag </span>响应标头值（响应数据的MD5签名）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r </span> </p> </td> 
   <td> <p>错误消息。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r </span> </p> </td> 
   <td> <p>从图像服务器检索缓存条目或数据所用的时间。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r </span> </p> </td> 
   <td> <p>请求解析和图像目录查找所花费的时间。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r </span> </p> </td> 
   <td> <p>指示此请求是否尝试在目录系统之外进行任何基于路径的访问。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r </span> </p> </td> 
   <td> <p>缓存群集中传递缓存项目的对等服务器的IP地址；如果<span class="codeph"> CacheUse </span>既不是<span class="codeph"> REMOTE_CREATED </span>也不是<span class="codeph"> REMOTE_UPDATED </span>，则为“ — ”。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r </span> </p> </td> 
   <td> <p>错误类别： </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=无错误。 </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=在服务器上找不到图像。 </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=IS协议使用错误或1以外的内容错误。 </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=其他服务器错误。 </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=请求因临时服务器过载而被拒绝。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r </span> </p> </td> 
   <td> <p><span class="codeph">请求的上限大小写值= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r </span> </p> </td> 
   <td> <p>请求主目录的根ID。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r </span> </p> </td> 
   <td> <p>将数据写入输出流后，[!DNL Platform Server]发送响应所需的时间。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r </span> </p> </td> 
   <td> <p>与<span class="codeph"> %B </span>类似，但包含304（未修改）响应的值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformedUrl}r </span> </p> </td> 
   <td> <p>所有规则集转换后的最终URL。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpRequestHeader </span>}i </span> </p> </td> 
   <td> <p>指定的HTTP请求标头的值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpResponseHeader </span>} </span> </p> </td> 
   <td> <p>指定的HTTP响应标头的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

默认值为`"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
