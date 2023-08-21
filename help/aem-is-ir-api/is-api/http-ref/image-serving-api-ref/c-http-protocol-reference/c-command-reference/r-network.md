---
title: nätverk
description: Lär dig hur du använder optimering av nätverksbandbredd för att justera den bildkvalitet som uppnås baserat på den faktiska nätverksbandbredden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# nätverk{#network}

Om du aktiverar nätverksbandbredd justeras den bildkvalitet som hanteras automatiskt baserat på den faktiska nätverksbandbredden. För dålig nätverksbandbredd [DPR (Device Pixel Ratio)](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) optimering inaktiveras automatiskt, även om det redan är aktiverat.

Om du vill kan ditt företag välja att inte optimera nätverksbandbredden på den enskilda bildnivån genom att lägga till `network=off` till bildens URL.

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> on|off </span> </p> </td> 
  <td class="stentry"> <p>Anger om nätverksbandbredden justerar bildkvaliteten som hanteras baserat på den faktiska nätverksbandbredden (på), eller om optimering av nätverksbandbredden är inaktiverat för att inte justera bildkvaliteten.</p> </td> 
 </tr> 
</table>

DPR- och nätverksbandbreddsvärdena baseras på de värden som identifierats på klientsidan för det paketerade CDN. Dessa värden är ibland felaktiga. IPhone5 med `dpr=2`och iPhone12 med `dpr=3`, båda visa `dpr=2`. För högupplösta enheter skickas ändå `dpr=2` är bättre än att skicka dpr=1. Det bästa sättet att överbrygga denna brist är dock att använda DPR på klientsidan för att ge er 100 % korrekta värden. Och det fungerar för alla enheter, oavsett om det är Apple eller någon annan enhet som startades. Se [Använd smart bildbehandling med enhetspixelproportioner på klientsidan](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## Egenskaper



## Standard

`network=off`

## Exempel

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## Se även

[drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Smart bildbehandling](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)