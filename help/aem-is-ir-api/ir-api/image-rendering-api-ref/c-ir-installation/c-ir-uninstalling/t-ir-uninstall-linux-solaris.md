---
title: 在Linux®和Solaris™上卸载
description: 按照以下说明在Linux®或Solaris™系统上卸载Image Rendering。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 6%

---

# 在Linux®和Solaris™上卸载{#uninstalling-on-linux-and-solaris}

按照以下说明在Linux®或Solaris™系统上卸载Image Rendering。 您可以使用两种不同的方法。 执行以下任一操作：

## 方法1

1. 查找 [!DNL uninstall.sh].

   它位于安装ImageRendering的目录中。 如果已删除此目录，则必须解压缩原始安装包，且不必提取 [!DNL uninstall.sh].
1. 运行 [!DNL uninstall.sh] 并按照屏幕上的说明进行操作。

## 方法2

1. 通过以下步骤停止ImageRendering:

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. 从系统中删除ImageRendering。 您使用的命令取决于您的系统。
   * Linux®: `rpm -e ImageRendering`

   * Solaris™: `pkgrm ImageRendering`

1. 删除步骤2中未删除的任何目录或文件。

