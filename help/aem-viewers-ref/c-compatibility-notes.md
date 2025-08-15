---
title: Kompatibilitetsinformation
description: Kompatibilitetsinformation för operativsystem, webbläsare och mobila enheter.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Kompatibilitetsinformation{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Kompatibilitetsinformation för operativsystem, webbläsare och mobila enheter.

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* Inkompatibelt med äldre adaptiva videouppsättningar. Ladda upp adaptiva videouppsättningar igen för att tillåta uppspelning.

## Allmänt {#section-7b9a9fcba85148d1802b7b3016b48e02}

* Skalning på webbläsarsidan gör användargränssnittet och bilderna suddiga när användaren zoomar in på sidan. Formateringen i användargränssnittet visas också felaktigt beroende på zoomning och överförs till helskärmsläge.
* På grund av storleksbegränsningen på mobila enheter använder visningsprogrammet för blandade media gester för att växla bildrutor i inbäddade bilduppsättningar i stället för att trycka på den inbäddade färgrutekomponenten. Komponenten finns som en visuell indikator.
* I Internet Explorer-webbläsare och vissa touchenheter upptar helskärmsläget inte hela enhetsskärmen. I stället ändras programmets storlek till webbläsarfönstrets storlek.
* Stängningsknappen fungerar inte i iOS 8.0 och iOS 8.1, men fungerar i iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Minnesläcka som kan ses i Zoom- och eCatalog-visningsprogram. Upprepad navigering genom bildrutor gör att webbläsaren kraschar.
* Om användaren dubbelknackar på ett visningsprogram zoomas hela sidan i stället för bara användaren när skalningen på webbläsarsidan är aktiverad.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Enheten har identifierats som en surfplatta i stående läge med helskärm incheckad i webbläsarinställningarna.

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Om användaren dubbelknackar på ett visningsprogram zoomas hela sidan i stället för bara användaren, och skalningen på webbläsarsidan aktiveras.

## Galaxy Nexus 10 och Galaxy {#section-ef52bd1249fe4f358c11838f7a557a00}

* I eCatalog visas felaktigt uppslag med stående och liggande orientering.

## HTML Mobile Devices {#section-dc42c80414c842e488738fc157c55b01}

* Oförmåga att inaktivera inbyggd nypning-zoom är en &quot;funktion&quot; i HTC UI-wrapper (HTC Sense). Den här funktionen kan göra att en hel sida zoomas när du använder&quot;nyp för att zooma&quot;-gesten i visningsprogrammet. Använd en dubbelknackningsgest i stället.
* Bildschemaikoner överlappar varandra om bildscheman är små och nära varandra.

## HTML5 Video Viewer {#section-3c2dd1220dea4093b17ca2dd0a688307}

* Modifieraren `IntialBitRate` stöds bara med uppspelning av HLS och Flash HDS. Det fungerar inte när uppspelningen använder den inbyggda spelaren.
* OGG- och WebM-progressiv uppspelning stöds inte.
* Webbläsarskalning gör att videospelaren visas i fel storlek (inklusive visningsinställningar för Kontrollpanelen i Windows®).
* Videosökningar med HLS-strömning på Safari är inkonsekventa.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Quirks-läget stöds inte.
* Kompatibilitetsläget stöds inte.
* Internet Explorer på mobilen stöds inte.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Stora e-kataloger gör att webbläsaren kraschar på iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 eller senare: Inställningarna för Internetplugin-program förhindrar uppspelning av Flash-video.
* Videosökningar med HLS-strömning på Safari är inkonsekventa.
* Det går inte att söka till slutet av en video på Safari 6 med HLS-strömning.
