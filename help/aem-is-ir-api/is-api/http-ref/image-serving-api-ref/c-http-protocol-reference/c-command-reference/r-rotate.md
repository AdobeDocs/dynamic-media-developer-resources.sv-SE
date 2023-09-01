---
title: rotera
description: Rotera bild. Roterar bild-, text- eller enfärgslagret med den angivna vinkeln.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# rotera{#rotate}

Rotera bild. Roterar bild-, text- eller enfärgslagret med den angivna vinkeln.

`rotate= *`vinkel`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> vinkel</span> </p> </td> 
  <td class="stentry"> <p>Rotationsvinkel i grader (reell). </p></td> 
 </tr> 
</table>

Positiva vinklar roterar medsols. Lagerfästpunkten ( `anchor=` eller `catalog::Anchor`) fungerar som centrum för rotation. Lagerrektangeln förstoras och monteras runt roterade data för att undvika beskärning. Rotationen används när lagrets bakgrundsområde fylls med `color=`. Modifieraren `bgColor=` kan användas för att lägga till bakgrundsfärg i markeringsramen efter rotation.

## Egenskaper {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

kommandot Lager. Gäller för det aktuella lagret eller för lagret 0 om `layer=comp`. Ignoreras av effektlager.

## Standard {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, utan rotering.

## Exempel {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

Placera etiketten&quot;Vid försäljning&quot; i det övre vänstra hörnet av bilder i en bildkatalog. Etikettbilden har redan rätt storlek för 300x300-vyn och bör roteras 30° åt vänster. Fyll textrutan med en vit halvogenomskinlig färg om du vill förbättra etiketten.

`http:// *`server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

Använd `size=` till lager 0 för att ange visningsstorlek, i stället för att använda `wid=` och `hei=`. Den här metoden tillåter `myImageId` som ska storleksändras utan att den slutliga storleken på `labelImage`. Ange också `scl=1`, annars kan den sammansatta bilden skalas till `attribute::DefaultPix` (om inte värdet är 0,0). Modifieraren `color=` lägger till den halvgenomskinliga bakgrundsfärgen i textrutan före rotering.

Nollpunkten för båda lagren ställs in på det övre vänstra hörnet för att uppnå den önskade justeringen. Ursprungspunkten för lager 1 gäller för `labelImage`när den har roterats.

Se [Exempel A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Mallar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) för ett exempel på roterad text.

## Se även {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
