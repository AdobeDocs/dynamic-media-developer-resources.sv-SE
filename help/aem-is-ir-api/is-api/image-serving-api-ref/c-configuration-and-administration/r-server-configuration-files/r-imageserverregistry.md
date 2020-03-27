---
description: Innehåller konfigurationsinställningar för Image Server.
seo-description: Innehåller konfigurationsinställningar för Image Server.
seo-title: ImageServerRegistry.xml
solution: Experience Manager
title: ImageServerRegistry.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: cc401f75-1eb1-40fe-8308-eaaf9e14f906
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ImageServerRegistry.xml{#imageserverregistry-xml}

Innehåller konfigurationsinställningar för Image Server.

När du ändrar den här XML-filen måste du se till att behålla giltig XML-syntax, annars kanske inte Image Server startar.

För att ändringarna ska börja gälla startar du om Image Server när du har redigerat den här filen. Det är bara elementvärdena som anges nedan som kan ändras. Redigera eventuellt annat innehåll i den här filen endast om du får råd från Scene7 Technical Support.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>Ändra inte elementens struktur `<imageserverregistry>`och ordning. Var försiktig när du redigerar den här filen, annars kanske inte Image Server kan startas.

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

Det kan finnas flera `<RootPath>` element (ett för varje källdatamapp). Image Server söker igenom rotsökvägarna i den ordning som anges för att hitta en viss källfil.
