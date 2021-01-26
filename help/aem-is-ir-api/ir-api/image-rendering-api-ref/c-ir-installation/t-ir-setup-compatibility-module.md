---
description: 必须设置和配置IR 3.x兼容模块。
seo-description: 必须设置和配置IR 3.x兼容模块。
seo-title: 设置和配置IR 3.x兼容性模块
solution: Experience Manager
title: 设置和配置IR 3.x兼容性模块
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 609a6ac9-1a4e-4cca-ab08-aa0f957b0e31
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 1%

---


# 设置和配置IR 3.x兼容模块{#setup-and-configure-ir-x-compatibility-module}

必须设置和配置IR 3.x兼容模块。

1. Stop `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. 更改到ImageServer Web应用程序目录。
1. 将[!DNL ir]目录的内容复制到[!DNL ROOT]目录中。
1. 在文本编辑器中打开[!DNL ROOT/WEB-INF/web.xml]。
1. 搜索行`<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. 取消`<servlet>`和`<servlet-mapping>`标记的注释。
1. 重新启动 `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux示例**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

然后，使用您最喜爱的编辑器编辑[!DNL web.xml]以取消`<servlet>`和`<servlet-mapping>`标记的注释。

**Windows示例**

打开资源管理器并转到`C:\Program Files\Scene7\ImageServing\webapps\ir`。

选择所有文件和文件夹，并复制`C:\Program Files\Scene7\ImageServing\webapps\ROOT`内的文件和文件夹。

然后，编辑文件`c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`，取消对`<servlet>`和`<servlet-mapping>`标记的注释。
