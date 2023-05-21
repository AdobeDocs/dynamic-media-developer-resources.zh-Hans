---
title: 字元編碼
description: 「影像演算」支援使用ISO-8859-1和UTF-8編碼的材質目錄。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# 字元編碼{#character-encoding}

「影像演算」支援使用ISO-8859-1和UTF-8編碼的材質目錄。

位元組順序標籤(BOM)可用來指定每個檔案的編碼。 對於UTF-8，BOM是位元組順序 `EF BB BF`. 在每個材質目錄檔案的開頭偵測到此字元序列時，會假設UTF-8編碼。 任何其他位元組序列都會導致檔案被解譯成ISO-8859-1標準。

許多當代應用程式在針對UTF-8進行配置時，會自動插入BOM。
