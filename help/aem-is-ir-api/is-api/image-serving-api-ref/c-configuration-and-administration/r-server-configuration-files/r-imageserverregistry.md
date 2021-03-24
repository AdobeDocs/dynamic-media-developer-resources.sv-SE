---
description: Innehåller konfigurationsinställningar för Image Server.
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# ImageServerRegistry.xml{#imageserverregistry-xml}

Innehåller konfigurationsinställningar för Image Server.

När du ändrar den här XML-filen måste du se till att behålla giltig XML-syntax, annars kanske inte Image Server startar.

För att ändringarna ska börja gälla startar du om Image Server när du har redigerat den här filen. Det är bara elementvärdena som anges nedan som kan ändras. Redigera allt annat innehåll i filen endast om Dynamic Media tekniska support rekommenderar det.

>[!NOTE]
>
>Ändra inte strukturen för `<imageserverregistry>`, inklusive ordningen för element. Var försiktig när du redigerar den här filen, annars kanske inte Image Server kan startas.

Följande visar vilka element som kan ändras. Det finns andra element som inte får ändras. Ordningen på elementen nedan återspeglar inte den ordning i vilken de måste finnas i filen.

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

## Anteckningar {#section-7217f011f69f41e7af4f3983d7776d6f}

Det kan finnas flera `<RootPath>`-element (ett för varje källdatamapp). Image Server söker igenom rotsökvägarna i den ordning som anges för att hitta en viss källfil.
