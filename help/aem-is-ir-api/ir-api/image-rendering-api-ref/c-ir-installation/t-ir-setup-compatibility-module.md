---
title: 設定和設定IR 3.x相容性模組
description: 設定並設定IR 3.x相容性模組。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 2%

---

# 設定和設定IR 3.x相容性模組{#setup-and-configure-ir-x-compatibility-module}

1. Stop `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. 變更至ImageServer webapps目錄。
1. 複製以下專案的內容： [!DNL ir] 目錄到 [!DNL `ROOT`] 目錄。
1. 開啟 [!DNL `ROOT/WEB-INF/web.xml`] 在文字編輯器中。
1. 搜尋行 `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. 取消註解 `<servlet>` 和 `<servlet-mapping>` 標籤之間。
1. 重新启动 `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux®範例**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

然後編輯 [!DNL `web.xml`] 使用您最愛的編輯器取消註解 `<servlet>` 和 `<servlet-mapping>` 標籤之間。

**Windows範例**

開啟檔案總管並前往 `C:\Program Files\Scene7\ImageServing\webapps\ir`.

選取所有檔案和資料夾，並複製其中的檔案和資料夾 `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

然後編輯檔案 `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`，取消註解 `<servlet>` 和 `<servlet-mapping>` 標籤之間。
