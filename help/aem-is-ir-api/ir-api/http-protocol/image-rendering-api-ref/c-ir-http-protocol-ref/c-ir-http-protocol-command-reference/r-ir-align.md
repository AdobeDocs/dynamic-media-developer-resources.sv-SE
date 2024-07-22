---
title: justera
description: Strukturåtergivningsjustering. Anger vilken av ursprungspunkterna som definieras av det markerade vinjetteringsobjektet som ska användas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---

# justera {#align}

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

Med renderaren används texturen på objektet så att texturens fästpunkt ( `anchor=`) sammanfaller med den angivna startpunkten.

Varje objekt kan definiera upp till sex nollpunkter (0, 1, 3, 4, 5, 6). Om ett `align`-värde anges men den motsvarande nollpunkten inte definieras av vinjettobjektet används standardstartpunkten (mittmatchningen).

`align=2` Anger slumpmässig texturjustering, i vilket fall `anchor=` ignoreras.

Används främst för möbelklädda material, möjligen för klädtyger, för att hantera justeringen av texturen mellan närliggande objekt.

## Egenskaper {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Materialattribut. Ignoreras om en vägg, ett skåp, en enhet eller ett fönstertäckningsobjekt har valts, eller om materialet inte är en upprepningsbar textur.

## Standard {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, om materialet är baserat på en katalogpost, annars 0 (centrerat-matchat).

## Se även {#section-945d1ce275df487d9d564d4043156c79}

[katalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
