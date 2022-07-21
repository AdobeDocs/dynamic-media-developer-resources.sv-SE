---
title: Systemkrav för visningsprogram för Dynamic Media HTML 5
description: Systemkrav för visningsprogram i Dynamic Media HTML 5.
solution: Experience Manager
contentOwner: Rick Brough
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: e4543358-92a6-4acc-a8a2-227e1daea722
source-git-commit: 8e09f8168987788f7d55849b4a275c488cfcc0b9
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Systemkrav för Dynamic Media HTML 5-visningsprogram{#system-requirements}

Systemkrav för visningsprogram i Dynamic Media HTML 5.

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Servermaskinvara och -programvara {#section-05099146f1f0418988c196635110bee6}

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

* Adobe Dynamic Media Image Serving 6.7.1 eller senare.
* HTML5-visningsprogram kräver SDK JavaScript-bibliotek på serversidan 3.11.5 eller senare.
* *Skicka e-post till en vän* sociala funktioner kräver s7ondemand 5.0.9 eller senare.
* eCatalog Viewer - [Popup för panelen Info](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-infopanelpopup.md) support kräver informationsserver 2.1.8 eller senare.
* Sökfunktionskomponenter kräver s7search 2.3.0 eller senare.

## Systemkrav för visningsprogram {#section-cc72b1e209524d038b4d5b92b35e998e}

**Lägsta krav för klientwebbläsare för komponentvisningsprogram:**

* Stöds på följande operativsystemversioner eller senare:
   * Microsoft® Windows® 7
   * macOS X 10.12
* Stöds i följande webbläsar-/plattformsversioner eller senare:
   * Android™ OS 4.x
   * BlackBerry® 10 i webbläsare. Endast videouppspelning stöds.
   * Krom 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS6
   * iPad 2 (endast webbläsarna Safari och Chrome)
   * iPhone 3GS
   * Safari 11
* Internet Explorer på mobila enheter stöds inte.
* *PanoramavyViewer* stöds i följande webbläsar-/plattformsversioner eller senare:
   * Android™ 4.4 (endast telefonenheter)
   * Krom 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11
* *Video360Viewer* och *DimensionalViewer* stöds i följande webbläsar-/plattformsversioner eller senare:
   * Android™ 5 (endast telefonenheter)
   * Krom 82
   * Edge
   * Firefox 77
   * iOS 12
   * Safari 12
* *ZoomVerticalViewer* stöds i följande webbläsar-/plattformsversioner eller senare:
   * Android™ 4.x
   * Krom 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11

**VIKTIGT**
Från och med 30 september 2022 upphör stödet för Dynamic Media-visningsprogram för Adobe att

* TLS (Transport Layer Security) 1.0 och 1.1
* Följande svaga lärare i TLS 1.2:
   * `TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384`
   * `TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA`
   * `TLS_RSA_WITH_AES_256_GCM_SHA384`
   * `TLS_RSA_WITH_AES_256_CBC_SHA256`
   * `TLS_RSA_WITH_AES_256_CBC_SHA`
   * `TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256`
   * `TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA`
   * `TLS_RSA_WITH_AES_128_GCM_SHA256`
   * `TLS_RSA_WITH_AES_128_CBC_SHA256`
   * `TLS_RSA_WITH_AES_128_CBC_SHA`
   * `TLS_RSA_WITH_CAMELLIA_256_CBC_SHA`
   * `TLS_RSA_WITH_CAMELLIA_128_CBC_SHA`
   * `TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA`
   * `TLS_RSA_WITH_SDES_EDE_CBC_SHA`

<!-- Effective September 30, 2018, Adobe Dynamic Media Classic Viewers ended support of Transport Layer Security 1.0 (TLS 1.0). As such, Dynamic Media Classic no longer supports viewers on the following browsers/platforms that support TLS 1.0 (Adobe recommends using TLS 1.2 or later):

* Android™ 2.3.7
* Android™ 4.0.4
* Android™ 4.1.1
* Android™ 4.2.2
* Android™ 4.3
* Internet Explorer 7 on Window Vista®
* Internet Explorer 8 on Windows® XP
* Internet Explorer 8-10 on Windows® 7
* Internet Explorer 10 on Windows® Phone 8.0
* Safari 5.1.9 on Apple OS X 10.6.8
* Safari 6.0.4 on Apple OS X 10.8.4
* Java™ 6u45
* Java™ 7u25
* OpenSSL 0.9.8y
* Baidu January 2015 -->

<!-- FLASH VIEWERS END-OF-LIFE — Effective January 31, 2017, Adobe Dynamic Media Classic officially ended support for the Flash viewer platform. -->
