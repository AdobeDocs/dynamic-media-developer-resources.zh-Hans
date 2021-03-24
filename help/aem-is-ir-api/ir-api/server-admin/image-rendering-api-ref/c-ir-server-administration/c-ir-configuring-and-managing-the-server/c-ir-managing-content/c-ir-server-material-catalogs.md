---
description: 材料目录提供许多图像渲染配置设置。
solution: Experience Manager
title: 材料目录
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# 材料目录{#material-catalogs}

材料目录提供许多图像渲染配置设置。

材料目录将请求中使用的晕影和材料ID映射到实际文件路径，可以存储与材料相关的所有元数据，并为模板提供容器。 他们跟踪ICC用户档案和命令宏。

材料目录只能通过图像渲染的Java组件访问（与Platform Server共同定位）。 目录属性文件必须具有[!DNL .ini]后缀并放在已注册的目录文件夹([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7))中。 默认材料目录([!DNL default.ini])必须始终存在，且必须填充所有属性才能正确运行图像服务。
