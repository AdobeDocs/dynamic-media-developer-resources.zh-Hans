---
title: 在Linux®和Solaris™上解除安裝
description: 請依照下列指示，在Linux®或Solaris™系統上解除安裝「影像演算」。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 6%

---

# 在Linux®和Solaris™上解除安裝{#uninstalling-on-linux-and-solaris}

請依照下列指示，在Linux®或Solaris™系統上解除安裝「影像演算」。 有兩種不同的方法可供您使用。 执行以下任一操作：

## 方法1

1. 查找 [!DNL uninstall.sh].

   它位於ImageRendering的安裝目錄中。 如果此目錄已移除，則必須解壓縮原始安裝套件並取消啟動以解壓縮 [!DNL uninstall.sh].
1. 執行 [!DNL uninstall.sh] 並依照熒幕上的指示操作。

## 方法2

1. 使用以下專案停止ImageRendering：

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. 從您的系統中移除ImageRendering。 您使用的指令取決於您的系統。
   * Linux®: `rpm -e ImageRendering`

   * Solaris™： `pkgrm ImageRendering`

1. 刪除步驟2中未移除的任何目錄或檔案。

