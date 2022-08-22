---
title: 设置和配置IR 3.x兼容模块
description: 设置并配置IR 3.x兼容模块。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 2%

---

# 设置和配置IR 3.x兼容模块{#setup-and-configure-ir-x-compatibility-module}

1. Stop `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. 更改为ImageServer Webapps目录。
1. 复制 [!DNL ir] 目录 [!DNL `ROOT`] 目录访问Advertising Cloud的帮助。
1. 打开 [!DNL `ROOT/WEB-INF/web.xml`] 在文本编辑器中。
1. 搜索行 `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. 取消注释 `<servlet>` 和 `<servlet-mapping>` 标记。
1. 重新启动 `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux®示例**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

然后编辑 [!DNL `web.xml`] 使用您喜爱的编辑器取消注释 `<servlet>` 和 `<servlet-mapping>` 标记。

**Windows示例**

打开资源管理器，然后转到 `C:\Program Files\Scene7\ImageServing\webapps\ir`.

选择所有文件和文件夹，并将其复制到 `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

然后编辑文件 `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`，取消注释 `<servlet>` 和 `<servlet-mapping>` 标记。
