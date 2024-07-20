---
title: 设置和配置IR 3.x兼容模块
description: 设置和配置IR 3.x兼容模块。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# 设置和配置IR 3.x兼容模块{#setup-and-configure-ir-x-compatibility-module}

1. 停止`<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`。
1. 转到ImageServer webapps目录。
1. 将[!DNL ir]目录的内容复制到[!DNL `ROOT`]目录中。
1. 在文本编辑器中打开[!DNL `ROOT/WEB-INF/web.xml`]。
1. 搜索行`<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. 取消注释`<servlet>`和`<servlet-mapping>`标记。
1. 重新启动`<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`。

**Linux®示例**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

然后，使用您喜爱的编辑器编辑[!DNL `web.xml`]以取消评论`<servlet>`和`<servlet-mapping>`标记。

**Windows示例**

打开资源管理器并转到`C:\Program Files\Scene7\ImageServing\webapps\ir`。

选择所有文件和文件夹并复制`C:\Program Files\Scene7\ImageServing\webapps\ROOT`中的文件和文件夹。

然后编辑文件`c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`，取消注释`<servlet>`和`<servlet-mapping>`标记。
