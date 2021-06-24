---
description: 包含图像服务器配置设置。
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 4483c5e8-5123-4d0f-bf9a-4ef8d8cec5a9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# ImageServerRegistry.xml{#imageserverregistry-xml}

包含图像服务器配置设置。

修改此XML文件时，必须注意维护有效的XML语法，否则图像服务器可能无法启动。

要使更改生效，请在编辑此文件后重新启动图像服务器。 仅支持修改下面列出的元素值。 仅在Dynamic Media技术支持部门提供建议时，才编辑此文件的任何其他内容。

>[!NOTE]
>
>请勿更改`<imageserverregistry>`的结构，包括元素的顺序。 编辑此文件时请务必谨慎，否则图像服务器可能无法启动。

下面说明了可以更改的元素。 其他元素也存在，不得更改。 以下元素的顺序并不反映它们在文件中必须存在的顺序。

```
<imageserverregistry>
    <TcpPort> 27345 </TcpPort>    
    <RootPath ./images </RootPath>
    <TempDirectory ./temp </TempDirectory>
    <Log> ./logs/ImageServer.log </Log>
    <TraceClient> 2 </TraceClient>
    <TraceStatsInterval> 600 </TraceStatsInterval>
    <PhysicalMemory> 20 </PhysicalMemory>
    <WorkerThreads> 0 </WorkerThreads>
    <SVGTcpPort> 27346 </SVGTcpPort>
    <MaxRenderRgnPixels> 16 </MaxRenderRgnPixels>
    <MaxSavePixels> 100 </MaxSavePixels>
    <MaxMessageSize> 16 </MaxMessageSize>
    <CacheServerUrl> http://localhost:8080/is/cache/secondary </CacheServerUrl>
    <NumberOfTextServers> 0 </NumberOfTextServers>
    <TextServerTcpPortRange> 27347-27380 </TextServerTcpPortRange>
    <SaveDirectory> ./ </SaveDirectory>
    <RemoteUrlDefaultExpiration> 36000 </RemoteUrlDefaultExpiration>
    <RemoteUrlTimeout> 60 </RemoteUrlTimeout>
    <MaxNonDsfSize> 4 </MaxNonDsfSize>
</imageserverregistry>
```

## 说明 {#section-7217f011f69f41e7af4f3983d7776d6f}

可能存在多个`<RootPath>`元素（每个源数据文件文件夹对应一个元素）。 图像服务器按指定的顺序搜索根路径以查找特定的源文件。
