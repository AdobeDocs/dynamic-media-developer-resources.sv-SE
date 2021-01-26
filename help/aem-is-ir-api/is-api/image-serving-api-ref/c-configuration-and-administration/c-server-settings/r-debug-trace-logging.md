---
description: Använd de här serverinställningarna för att felsöka spårningsloggning.
seo-description: Använd de här serverinställningarna för att felsöka spårningsloggning.
seo-title: Debug_trace-loggning
solution: Experience Manager
title: Debug_trace-loggning
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 33f1d093-007d-453b-965a-9d701a845954
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# Debug_trace-loggning{#debug-trace-logging}

Använd de här serverinställningarna för att felsöka spårningsloggning.

>[!NOTE]
>
>Vi rekommenderar att du konfigurerar alla loggfiler som ska skrivas till samma mapp som `TC::directory`. Detta garanterar att alla loggfiler för Image Serving deltar i den automatiska loggfilsrotationen som konfigurerats med `TC::maxDays`, vilket förhindrar att servern blir instabil på grund av att det inte finns tillräckligt med diskutrymme.

## SV::log - Sökväg till loggfil för serveradministratörens spårningslogg {#section-3697bc480ff646e79cacc2812c55ef26}

Mapp- och basfilnamn för Server Supervisor-loggfiler. Sökvägen kan vara absolut eller relativ till *[!DNL install_folder]*. Serverhanteraren lägger till ett bindestreck och det aktuella datumet ( *[!DNL -yyyy-mm-dd]*) till filnamnet (före filsuffixet, om det finns något). Vi rekommenderar att du skickar alla loggfiler till samma mapp som loggfilerna för plattformsservern ( `PS::LogFolder`) för att utnyttja loggfilshanteringen som implementeras av plattformsservern ( `PS::LogDays`). Standardvärdet är [!DNL logs/Supervisor.log].

>[!NOTE]
>
>Den nya mappen måste skapas innan den här inställningen ändras. Se till att åtkomstbehörigheterna är inställda så att Serverhanteraren har de nödvändiga behörigheterna för att skapa, läsa och skriva.

## SV::trachel - Loggnivå för servertillsynsspårning {#section-36f8634741da4c618d67aa628b5fe474}

Loggnivån kan vara 1, 2, 3 eller 4. Standardvärdet är 2.

## IS::Log - Felsökningsloggfilssökväg för Image Server {#section-73a3f09b77f2446c9f82207b7d8aec39}

Mapp- och basfilnamn för bildserverns spårningsloggfiler. Sökvägen kan vara absolut eller relativ till *[!DNL install_folder]*. ImageServer lägger till ett bindestreck och det aktuella datumet ( *[!DNL -yyyy-mm-dd]*) till filnamnet (före filsuffixet, om det finns något). Vi rekommenderar att du skickar loggfiler för Image Server till samma mapp som loggfilerna för Platform Server ( `PS::LogFolder`) för att utnyttja loggfilshanteringen som implementeras av Platform Server (se `PS::LogDays`).

>[!NOTE]
>
>Den nya mappen måste skapas innan den här inställningen ändras. Kontrollera att åtkomstbehörigheterna är inställda så att Image Serving har de nödvändiga behörigheterna för att skapa, läsa och skriva.

## IS:TraceClient - Felsökningsloggnivå för bildserver {#section-3851f1f68e404430985c629ac80534db}

Loggnivån kan vara 1, 2, 3 eller 4 (standard är 2)

Nivå 1 loggar händelser relaterade till anslutningar för start, avstängning och plattformsserver.

Nivå 2 loggar även anslutning till och frånkoppling från källbilder.

Nivå 3 lägger till loggning av begäranden om pixeldata och leverans av dessa till plattformsservern.

Nivå 4 registrerar alla meddelanden som tagits emot från plattformsservern.

Nivå 3 och 4 bör endast användas i felsökningssyfte eftersom loggfilerna kan bli mycket stora.

## IS::TraceStatsInterval - Loggintervall för bildserverstatistik {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Image Server skriver minnesstatistik till sin spårningsloggfil med det intervall som anges av den här inställningen. Giltigt intervall är 5 till 86 400 sekunder.
