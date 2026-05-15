---
description: 图像蒙版。 请求掩码（Alpha通道）数据。
solution: Experience Manager
title: 蒙版
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
TQID: 'https://experienceleague.adobe.com/FMsQMZsc3N1ToEzXBE0vOzkezfemSzT6NaGJQ1gQqd8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# 蒙版{#mask}

图像蒙版。 请求掩码（Alpha通道）数据。

`req=mask`

支持与`req=img`相同的命令。 服务器以相同的方式处理，但服务器不会返回RGB或RGBA数据，而是丢弃颜色信息并仅返回蒙版（alpha通道）数据。 回复数据格式和响应MIME类型由`fmt=`确定。

可使用基于`catalog::Expiration`的TTL来缓存HTTP响应。
