---
description: 包含图像服务器配置设置。
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4483c5e8-5123-4d0f-bf9a-4ef8d8cec5a9
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# ImageServerRegistry.xml{#imageserverregistry-xml}

包含图像服务器配置设置。

修改此XML文件时，必须注意保持有效的XML语法，否则图像服务器可能无法启动。

要使更改生效，请在编辑此文件后重新启动图像服务器。 仅支持修改下面列出的元素值。 仅当Dynamic Media技术支持提供建议时，才编辑此文件的任何其他内容。

>[!NOTE]
>
>不要更改的结构 `<imageserverregistry>`，包括元素的顺序。 编辑此文件时请务必小心，否则图像服务器可能会无法启动。

下面说明了哪些元素可以更改。 存在不能更改的其他元素。 以下元素的顺序并不能反映它们在文件中必须存在的顺序。

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

多个 `<RootPath>` 元素可能存在（每个源数据文件文件夹一个）。 图像服务器按指定的顺序搜索根路径，以查找特定的源文件。
