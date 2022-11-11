---
description: 材料目录提供了许多“图像渲染”配置设置。
solution: Experience Manager
title: 材料目录
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 材料目录{#material-catalogs}

材料目录提供了许多“图像渲染”配置设置。

材料目录将请求中使用的晕影和材料ID映射到实际文件路径，可以存储与材料相关的所有元数据，并为模板提供容器。 它们跟踪ICC配置文件和命令宏。

材料目录仅由“图像渲染”的Java组件访问(与 [!DNL Platform Server])。 目录属性文件必须具有 [!DNL .ini] 后缀并放在注册的目录文件夹([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7))。 默认材料目录( [!DNL default.ini])必须始终存在，且必须填充所有属性，才能正确使用图像服务。
