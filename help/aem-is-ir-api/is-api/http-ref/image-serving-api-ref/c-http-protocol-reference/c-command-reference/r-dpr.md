---
title: dpr
description: Enhetens pixelproportioner (DPR)&mdash;also known as CSS pixel ratio&mdash;is the relationship between a device's physical pixels and logical pixels.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d64ca9ed-7d8e-4a13-9c9d-acb7de3e31ed
source-git-commit: 63c0e3b494b6d583117dad01643946900855802e
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 1%

---

# dpr{#dpr}

Device Pixel Ratio (DPR) - även kallat CSS-pixelförhållande - är relationen mellan en enhets fysiska pixlar och logiska pixlar. I synnerhet med nya retinaskärmar växer pixelupplösningen i moderna mobilenheter i snabb takt.

Om du aktiverar optimering av enhetspixelproportioner återges bilden med skärmens ursprungliga upplösning, vilket gör den skarp.

För närvarande kommer bildskärmens pixeldensitet från Akamai CDN-rubrikvärden.

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> av </span> </span> </p> </td> 
  <td class="stentry"> <p>Inaktivera DPR-optimering på URL-nivå för en enskild bild. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> on, dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>Åsidosätt det DPR-värde som identifieras av Smart Imaging, med ett anpassat värde (som identifieras av någon klientlogik eller annan metod). Tillåtet värde för dprValue är ett tal som är större än 0. </p> </td> 
 </tr> 
</table>


Du kan använda `dpr=on,dprValue` även om DPR-inställningen på företagsnivå är inaktiverad.

På grund av DPR-optimering identifieras alltid MaxPix-bredden när den resulterande bilden är större än Dynamic Media-inställningen MaxPix genom att bildens proportioner behålls.

| Begärd bildstorlek | DPR-värde | Levererad bildstorlek |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2 448 x 1 500 |
| 816 x 500 | 4 | 3264 x 2000 |

DPR-värdena baseras på de värden som identifierats på klientsidan för det paketerade CDN. Dessa värden är ibland felaktiga. IPhone5 med `dpr=2` och iPhone12 med dpr=3 visar båda `dpr=2`. För högupplösta enheter är det ändå bättre att skicka `dpr=2` än att skicka `dpr=1`. Det bästa sättet att överbrygga denna brist är dock att använda DPR på klientsidan för att ge er 100 % korrekta värden. Och det fungerar för alla enheter, oavsett om det är Apple eller någon annan enhet som startades. Se [Använd smart bildbehandling med enhetspixelproportioner på klientsidan](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## Egenskaper

Ett request-attribut. Det har ingen effekt om `dpr` är av eller om `dprValue=1`.

## Standard

`dpr=off`


## Exempel

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## Se även

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [nätverk](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [Smart bildbehandling](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)
