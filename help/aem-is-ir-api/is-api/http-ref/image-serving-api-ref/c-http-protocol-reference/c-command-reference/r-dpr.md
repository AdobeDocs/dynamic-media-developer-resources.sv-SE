---
title: dpr
description: Enhetens pixelproportioner (DPR)&mdash; kallas även CSS-pixelkvot&mdash;är relationen mellan en enhets fysiska pixlar och logiska pixlar.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '219'
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


Du kan använda `dpr=on,dprValue` även om företagets nivå DPR-inställning är avstängd.

På grund av DPR-optimering identifieras alltid MaxPix-bredden när den resulterande bilden är större än Dynamic Media-inställningen MaxPix genom att bildens proportioner behålls.

| Begärd bildstorlek | DPR-värde | Levererad bildstorlek |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2 448 x 1 500 |
| 816 x 500 | 4 | 3264 x 2000 |

## Egenskaper



## Standard

`dpr=off`


## Exempel

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## Se även

[nätverk](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [Smart bildbehandling](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)