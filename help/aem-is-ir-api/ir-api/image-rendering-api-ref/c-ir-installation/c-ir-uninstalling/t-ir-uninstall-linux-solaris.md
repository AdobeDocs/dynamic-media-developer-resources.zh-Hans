---
title: 在Linux®和Solaris™上卸载
description: 按照以下说明在Linux®或Solaris™系统上卸载“Image Rendering（图像渲染）”。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# 在Linux®和Solaris™上卸载{#uninstalling-on-linux-and-solaris}

按照以下说明在Linux®或Solaris™系统上卸载“Image Rendering（图像渲染）”。 您可以使用两种不同的方法。 执行以下任一操作：

## 方法1

1. 查找[!DNL uninstall.sh]。

   它位于ImageRendering的安装目录中。 如果此目录已被删除，则必须解压缩原始安装包并取消其分段才能提取[!DNL uninstall.sh]。
1. 运行[!DNL uninstall.sh]并按照屏幕上的说明操作。

## 方法2

1. 使用以下内容停止ImageRendering：

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. 从系统中删除ImageRendering。 使用的命令取决于您的系统。
   * Linux®： `rpm -e ImageRendering`

   * Solaris™： `pkgrm ImageRendering`

1. 删除步骤2中未删除的任何目录或文件。

