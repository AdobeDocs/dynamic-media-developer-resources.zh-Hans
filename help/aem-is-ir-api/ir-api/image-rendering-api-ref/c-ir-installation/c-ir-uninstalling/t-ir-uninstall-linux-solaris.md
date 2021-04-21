---
description: 按照以下说明卸载Linux或Solaris系统上的图像渲染。
solution: Experience Manager
title: 在Linux和Solaris上卸载
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---


# 在Linux和Solaris上卸载{#uninstalling-on-linux-and-solaris}

按照以下说明卸载Linux或Solaris系统上的图像渲染。

在Linux或Solaris系统上卸载图像渲染有两种方法。

**方法1**

1. 查找 [!DNL uninstall.sh].

   它位于安装ImageRendering的目录中。 如果此目录已被删除，则必须解压缩原始安装包并取消其目标以解压[!DNL uninstall.sh]。
1. 运行[!DNL uninstall.sh]并按照屏幕上的说明操作。

>**方法2**
>
>1. 通过以下方式停止图像渲染：` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. 从您的系统中删除图像渲染。

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



