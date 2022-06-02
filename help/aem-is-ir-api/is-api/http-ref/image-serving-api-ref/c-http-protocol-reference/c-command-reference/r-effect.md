---
title: effekt
description: Välj Effektlager. Markerar ett effektlager och startar ett nytt lagersegment i strängen för begäran, som är associerad med det aktuella lagret.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# effekt{#effect}

Välj Effektlager. Markerar ett effektlager och startar ett nytt lagersegment i strängen för begäran, som är associerad med det aktuella lagret.

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>Effektlagrets nummer (inte lika med 0). </p></td> 
 </tr> 
</table>

Alla kommandon i det nya segmentet används på det angivna effektlagret. Ett effektlagersegment avslutas av nästa `layer=` eller `effect=` eller i slutet av begäran.

*`n`* måste vara mindre än 0 för yttre lagereffekter (dvs. effekter bakom det överordnade lagret) och större än 0 för inre lagereffekter (dvs. effekter i det överordnade lagret). Effektlagrets nummer behöver inte följa på varandra.

Effektlagrets nummer anger z-ordningen, om det finns flera effektlager för samma överordnade lager. Lager med högre nummer placeras ovanpå lager med lägre nummer.

Effektlager kan kopplas till `layer=comp`.

## Egenskaper {#section-e11f795deff345779ce280a82cf221ca}

Effektlager, kommando. *`n`* får inte vara 0.

## Standard {#section-84bbe1cfe7a94040827c994323ac59d4}

Ingen.

## Exempel {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## Se även {#section-573273e9e0e64103a5764075f5e50180}

[layer=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)
