---
description: 按照以下说明在Linux或Solaris系统上卸载图像渲染。
seo-description: 按照以下说明在Linux或Solaris系统上卸载图像渲染。
seo-title: 在Linux和Solaris上卸载
solution: Experience Manager
title: 在Linux和Solaris上卸载
topic: Scene7 Image Serving - Image Rendering API
uuid: 80c0d6ec-985b-4596-bd67-22e5029f7b37
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 在Linux和Solaris上卸载{#uninstalling-on-linux-and-solaris}

按照以下说明在Linux或Solaris系统上卸载图像渲染。

在Linux或Solaris系统上卸载图像渲染有两种方法。

**方法1**

1. 查找 [!DNL uninstall.sh].

   它位于安装ImageRendering的目录中。 如果此目录已被删除，则必须解压缩原始安装包并取消其目标以解压 [!DNL uninstall.sh]。
1. 运 [!DNL uninstall.sh] 行并按照屏幕上的说明操作。
>**方法2**
>
>1. 通过以下方式停止图像渲染： ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. 从系统中删除ImageRendering。
>
>   
删除ImageRendering的命令取决于您的系统：
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris: `pkgrm ImageRendering`
>
>1. 删除步骤2中未删除的任何目录或文件。
>



