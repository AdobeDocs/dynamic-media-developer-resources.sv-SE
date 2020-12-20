---
description: Använd de här serverinställningarna för att konfigurera servern.
seo-description: Använd de här serverinställningarna för att konfigurera servern.
seo-title: Server
solution: Experience Manager
title: Server
topic: Scene7 Image Serving - Image Rendering API
uuid: 50db98cc-8354-4884-9416-00808828061b
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---


# Server{#server}

Använd de här serverinställningarna för att konfigurera servern.

## SV::ImageServerMode - Image Server Mode {#section-991b287f2dde4f77a24fc69d5b32cabd}

Både en 32- och en 64-bitarsversion av Image Server finns för Linux. Ange ImageServer64 när den installeras på 64-bitars Linux-servrar, eller ImageServer32 (standard) när den installeras på 32-bitarsservrar.

>[!NOTE]
>
>64-bitarsversionen av Image Server stöder inte FlashPix-källfiler.

>[!NOTE]
>
>64-bitarsläge stöds inte i Windows. Endast `ImageServer32` kan anges. I annat fall startar inte Image Serving.

## SV::PSHeapSize - stackstorlek för plattformsserver {#section-fd83715948764aeda58d6b3a9f9f8be9}

Java-stackstorleken för plattformsservern. Standardvärdet är `512m` (512 MB).

## IS::TcpPort, PS::isConnection.port - Image Server Listening Port {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Anger porten som används för kommunikation mellan plattformsservern och Image-servern. Se till att ange ett portnummer som inte används på annat sätt på värdsystemet.

>[!NOTE]
>
>För att Image Serving ska fungera på rätt sätt måste samma värde anges för `IS::TcpPort` och `PS::isConnection.port`.

## IS::PhysicalMemory - Minnesgräns för avbildningsserver {#section-85e37aa2ac6e456eb698da716dd3247d}

Den ungefärliga gränsen för bilddata i minnet, uttryckt i procent av det fysiska minnet. Giltigt intervall är 10 till 90 %. Image Server försöker begränsa användningen av bildminne till den angivna mängden om möjligt. Gränsen får överskridas tillfälligt under omfattande bearbetning.

## IS::WorkerThreads - Antal arbetstrådar för Image Server {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Det maximala antalet trådar som Image Server använder för bearbetning av bilddata. Standardvärdet är 0, vilket gör att Image Server automatiskt kan optimera antalet trådar.

Vissa operativsystem har kopplingsmodeller med hög kontextväxling. I sådana fall kan serverprestanda förbättras när ett visst antal trådar väljs (t.ex. en tråd per CPU). Det kan krävas vissa försök för att hitta den optimala inställningen. Mer information finns i versionsinformationen för Image Serving och i dokumentationen för operativsystemet.

## IS::NumberOfTextServers - Antal textserverinstanser {#section-971e20a90c1a473598fba738ed95671a}

Det maximala antalet textrenderare som ska vara aktiva samtidigt. 0 (standard) motsvarar 1,5 gånger antalet tillgängliga processorkärnor.

## IS::TextServerTcpPortRange - Kommunikationsportar för textserver {#section-a13465de88ed4df09931e5ba840c1942}

Portarna som ska användas för textserverkommunikation. Ange det första och sista portnumret, avgränsat med &#39;-&#39;.
