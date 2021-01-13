---
description: Kompatibilitetsinformation för operativsystem, webbläsare och mobila enheter.
seo-description: Kompatibilitetsinformation för operativsystem, webbläsare och mobila enheter.
seo-title: Kompatibilitetsanteckningar
solution: Experience Manager
title: Kompatibilitetsanteckningar
topic: Dynamic media
uuid: cf732a03-bfaa-4838-862f-73343cefbd67
translation-type: tm+mt
source-git-commit: 07eb6cf84a46753b41307187d5c5b2a077fa9009
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---


# Kompatibilitetsinformation{#compatibility-notes}

<!-- Updated January 13,2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Kompatibilitetsinformation för operativsystem, webbläsare och mobila enheter.

## Blackberry {#section-0c465ac3775d47fd838e2695a00abc45}

* Inkompatibelt med äldre adaptiva videouppsättningar. Du kan behöva överföra adaptiva videouppsättningar igen för att tillåta uppspelning.

## Allmänt {#section-7b9a9fcba85148d1802b7b3016b48e02}

* Skalning på webbläsarsidan kan göra användargränssnittet och bilderna suddiga när användaren zoomar in på sidan. Gränssnittsformatering kan också visas felaktigt beroende på zoomning. Detta kommer att överföras till helskärm.
* På grund av storleksbegränsningen på mobila enheter använder Mixed Media Viewer glidningsgest för att växla bildrutor i inbäddade bilduppsättningar i stället för att trycka på den inbäddade färgrutekomponenten. Komponenten finns som en visuell indikator.
* I Internet Explorer-webbläsare och vissa touchenheter upptar helskärmsläget inte hela enhetsskärmen. I stället ändras programmets storlek till webbläsarfönstrets storlek.
* Stängningsknappen fungerar inte i iOS 8.0 och iOS 8.1, men fungerar i iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Minnesläcka som kan ses i Zoom- och eCatalog-visningsprogram. Upprepad navigering i bildrutor kan göra att webbläsaren kraschar.
* Dubbelknackning på ett visningsprogram kan göra att hela sidan zoomas i stället för bara användaren som har skalning på webbläsaren aktiverad.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Enheten identifieras som en surfplatta i stående läge med helskärm markerat i webbläsarinställningarna.

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Dubbeltryck på ett visningsprogram kan göra att hela sidan zoomas i stället för bara användaren, med skalning på webbläsarsidan aktiverad.

## Galaxy Nexus 10 och Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* I eCatalog visas felaktigt uppslag med stående och liggande orientering.

## HTML Mobile Devices {#section-dc42c80414c842e488738fc157c55b01}

* Oförmåga att inaktivera inbyggd nypning-zoom är en &quot;funktion&quot; i HTC UI-wrapper (HTC Sense). Den här funktionen kan göra att en hel sida zoomas när du använder&quot;nyp för att zooma&quot;-gesten i visningsprogrammet. Använd en dubbelknackningsgest i stället.
* Bildschemaikoner kan överlappa om bildscheman är små och nära varandra.

## HTML5 Video Viewer {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` modifierare stöds bara med programvaru-HLS och Flash HDS-uppspelning. Det fungerar inte när uppspelningen använder den inbyggda spelaren.
* OGG- och WebM-progressiv uppspelning stöds inte.
* Webbläsarskalning kan göra att videospelaren visas i fel storlek (inklusive visningsinställningar för Windows OS-kontrollpanelen).
* Videosökning med HLS-strömning på Safari kan vara inkonsekvent.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Quirks-läget stöds inte.
* Kompatibilitetsläget stöds inte.
* Internet Explorer på mobilen stöds inte.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Stora e-kataloger kan få webbläsaren att krascha på iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 eller senare: Inställningarna för Internetplugin-programmet kan förhindra uppspelning av Flash-video.
* Videosökning med HLS-strömning på Safari kan vara inkonsekvent.
* Det går inte att söka till slutet av videon på Safari 6 med HLS-direktuppspelning.
