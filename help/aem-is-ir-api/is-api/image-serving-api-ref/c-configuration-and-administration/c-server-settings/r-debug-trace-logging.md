---
title: Debug_trace-loggning
description: Använd de här serverinställningarna för att felsöka spårningsloggning.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Debug_trace-loggning{#debug-trace-logging}

Använd de här serverinställningarna för att felsöka spårningsloggning.

>[!NOTE]
>
>Adobe rekommenderar att du konfigurerar alla loggfiler som ska skrivas till samma mapp som `TC::directory`. På så sätt säkerställer du att alla loggfiler i Image Serving deltar i den automatiska loggfilsrotationen som konfigurerats med `TC::maxDays`som förhindrar att servern blir instabil på grund av att det inte finns tillräckligt med diskutrymme.

## SV::log - Sökväg till loggfil för serveradministratörens spårningslogg {#section-3697bc480ff646e79cacc2812c55ef26}

Mapp- och basfilnamn för Server Supervisor-loggfiler. Sökvägen kan vara absolut eller relativ till *[!DNL install_folder]*. Server Supervisor lägger till ett bindestreck och det aktuella datumet ( *[!DNL -yyyy-mm-dd]*) till filnamnet (före eventuella filsuffix). Adobe rekommenderar att du skickar alla loggfiler till samma mapp som [!DNL Platform Server] loggfiler ( `PS::LogFolder`) för att använda den loggfilshantering som implementeras av [!DNL Platform Server] (`PS::LogDays`). Standardvärdet är [!DNL logs/Supervisor.log].

>[!NOTE]
>
>Den nya mappen måste skapas innan den här inställningen ändras. Se till att åtkomstbehörigheterna är inställda så att Serverhanteraren har de nödvändiga behörigheterna för att skapa, läsa och skriva.

## SV::trachel - Loggnivå för servertillsynsgrupp {#section-36f8634741da4c618d67aa628b5fe474}

Loggnivån kan vara 1, 2, 3 eller 4. Standardvärdet är 2.

## IS::Log - Felsökningsloggfilens sökväg för Image Server {#section-73a3f09b77f2446c9f82207b7d8aec39}

Mapp- och basfilnamn för bildserverns spårningsloggfiler. Sökvägen kan vara absolut eller relativ till *[!DNL install_folder]*. ImageServer lägger till ett bindestreck och det aktuella datumet ( *[!DNL -yyyy-mm-dd]*) till filnamnet (före eventuella filsuffix). Adobe rekommenderar att du skickar loggfiler för Image Server till samma mapp som [!DNL Platform Server] loggfiler ( `PS::LogFolder`) för att använda den loggfilshantering som implementeras av [!DNL Platform Server] (se `PS::LogDays`).

>[!NOTE]
>
>Den nya mappen måste skapas innan den här inställningen ändras. Kontrollera att åtkomstbehörigheterna är inställda så att Image Serving har de nödvändiga behörigheterna för att skapa, läsa och skriva.

## IS:TraceClient - Felsökningsloggnivå för bildserver {#section-3851f1f68e404430985c629ac80534db}

Loggnivån kan vara 1, 2, 3 eller 4 (standard är 2)

Nivå 1 loggar händelser som rör start, avstängning och [!DNL Platform Server] anslutningar.

Nivå 2 loggar även anslutning till och frånkoppling från källbilder.

Nivå 3 lägger till loggning av begäranden om pixeldata och leverans av samma till [!DNL Platform Server].

Nivå 4 registrerar alla meddelanden som tagits emot från [!DNL Platform Server].

Nivå 3 och 4 bör endast användas i felsökningssyfte eftersom loggfilerna kan bli stora.

## IS::TraceStatsInterval - Loggintervall för bildserverstatistik {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Image Server skriver minnesstatistik till sin spårningsloggfil med det intervall som anges av den här inställningen. Det giltiga intervallet är 5-86 400 sekunder.
