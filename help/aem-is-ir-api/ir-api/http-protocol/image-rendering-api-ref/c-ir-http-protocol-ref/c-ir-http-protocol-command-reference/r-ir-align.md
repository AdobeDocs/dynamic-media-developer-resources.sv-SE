---
description: Strukturåtergivningsjustering. Anger vilken av ursprungspunkterna som definieras av det markerade vinjetteringsobjektet som ska användas.
seo-description: Strukturåtergivningsjustering. Anger vilken av ursprungspunkterna som definieras av det markerade vinjetteringsobjektet som ska användas.
seo-title: justera
solution: Experience Manager
title: justera
topic: Scene7 Image Serving - Image Rendering API
uuid: 0b24cd82-f9b2-48f4-9052-8c2026370ff7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# justera{#align}

Strukturåtergivningsjustering. Anger vilken av ursprungspunkterna som definieras av det markerade vinjetteringsobjektet som ska användas.

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Standardstartpunkt (mittmatchning). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Löpande matchningsursprung. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Slumpmässig justering. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3..6 </p></td> 
  <td class="stentry"> <p>Användardefinierad ursprung. </p></td> 
 </tr> 
</table>

Med renderaren tillämpas texturen på objektet så att texturens fästpunkt ( `anchor=`) sammanfaller med den angivna startpunkten.

Varje objekt kan definiera upp till 6 punkter (0,1, 3, 4, 5, 6). Om ett `align` värde anges men motsvarande nollpunkt inte definieras av vinjettobjektet, används standardnollpunkten (mittmatchningen).

`align=2` anger slumpmässig texturjustering, i vilket fall `anchor=` ignoreras.

Används främst för möbelklädda material, möjligen för klädtyger, för att hantera justeringen av texturen mellan närliggande objekt.

## Egenskaper {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Materialattribut. Ignoreras om en vägg, ett skåp, en enhet eller ett fönstertäckningsobjekt har valts, eller om materialet inte är en upprepningsbar textur.

## Standard {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, om materialet är baserat på en katalogpost, annars 0 (centrerat).

## Se även {#section-945d1ce275df487d9d564d4043156c79}

[katalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
