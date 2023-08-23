---
title: nätverk
description: Lär dig hur du använder optimering av nätverksbandbredd för att justera den bildkvalitet som uppnås baserat på den faktiska nätverksbandbredden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 96b60fd5f6e3550993cd7640138df4c9bbf6b955
workflow-type: tm+mt
source-wordcount: '145'
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

Värdena för nätverksbandbredd baseras på de värden som identifierats på klientsidan för det paketerade CDN.

## Egenskaper



## Standard

`network=off`

## Exempel

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## Se även

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Smart bildbehandling](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)