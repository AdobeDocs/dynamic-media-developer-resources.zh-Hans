---
title: 在Linux®和Solaris™上卸载
description: 按照以下说明在Linux®或Solaris™系统上卸载“Image Rendering（图像渲染）”。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
TQID: 'https://experienceleague.adobe.com/RmD5z5300Nw12kSsOretyAl5p-TeFkox-Cyqm1MrF5w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 120
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


