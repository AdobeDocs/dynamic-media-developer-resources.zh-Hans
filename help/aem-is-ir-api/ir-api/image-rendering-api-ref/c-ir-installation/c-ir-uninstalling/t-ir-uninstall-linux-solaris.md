---
description: 按照以下说明在Linux或Solaris系统上卸载Image Rendering。
solution: Experience Manager
title: 在Linux和Solaris上卸载
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---

# 在Linux和Solaris上卸载{#uninstalling-on-linux-and-solaris}

按照以下说明在Linux或Solaris系统上卸载Image Rendering。

在Linux或Solaris系统上卸载Image Rendering的方法有两种。

**方法1**

1. 查找 [!DNL uninstall.sh].

   它位于安装ImageRendering的目录中。 如果已删除此目录，则必须解压缩原始安装包，且不必使用该目录来提取[!DNL uninstall.sh]。
1. 运行[!DNL uninstall.sh]并按照屏幕上的说明操作。

>**方法2**
>
>1. 通过以下方式停止ImageRendering:` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. 从系统中删除ImageRendering。

>
>   
删除ImageRendering的命令取决于您的系统：
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris:`pkgrm ImageRendering`
>
>1. 删除步骤2中未删除的任何目录或文件。

>


