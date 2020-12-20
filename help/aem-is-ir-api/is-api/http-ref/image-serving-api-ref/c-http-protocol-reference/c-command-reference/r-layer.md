---
description: Välj Lager. Markerar ett lager och startar ett nytt lagerdefinitionssegment i kommandosekvensen.
seo-description: Välj Lager. Markerar ett lager och startar ett nytt lagerdefinitionssegment i kommandosekvensen.
seo-title: lager
solution: Experience Manager
title: lager
topic: Scene7 Image Serving - Image Rendering API
uuid: 882309b3-51d7-477e-bd09-068ce9e55eb5
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---


# lager{#layer}

Välj Lager. Markerar ett lager och startar ett nytt lagerdefinitionssegment i kommandosekvensen.

`layer= *``*|comp[, *`name`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>Antal lager som ska markeras (0 eller större int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> skiss</span> </p></td> 
  <td class="stentry"> <p>Markera den sammansatta bilden. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p></td> 
  <td class="stentry"> <p>Lagernamn. </p></td> 
 </tr> 
</table>

Alla kommandon i lagersegmentet används på det angivna lagret. Ett lagersegment avslutas av nästa `layer=`- eller `effect=`-kommando eller slutet av begäran.

Ange `layer=comp` om du vill markera den sammansatta bilden (eller visa vissa kommandon).

Lagernumret anger effektivt z-ordningen för lagret. Lager med högre nummer placeras ovanpå lager med lägre nummer.

Lagernummer behöver inte vara i följd. Lager 0 krävs.

Ett namn kan tilldelas ett lager med kommandovarianten `layer= *`n`*, *`name`*`. När ett namngivet lager har definierats kan det refereras till med ` layer= *`namn`*`, utan att behöva känna till lagrets nummer. Flera namn kan tilldelas till samma lager med flera `layer= *`n`*, *`name`*`-kommandon.

>[!NOTE]
>
>Lager 0 anger den totala storleken på den sammansatta arbetsytan. Alla delar av lager som ligger utanför gränserna för lager 0 beskärs när det sammansatta lagret byggs.

## Egenskaper {#section-499963ee52c14f2898f0d0f90c1d01be}

Lager, kommando. Ersättningsvariabelreferenser stöds inte i `layer=`.

`comp` tillåts inte som en  *`name`* sträng. Ett fel returneras om samma *`name`* har tilldelats till mer än ett lager, eller om *`name`* refererar till ett lager som inte har definierats tidigare.

## Standard {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. Många kommandon och attribut gäller för lager 0 om `layer=comp`.

## Specialfall {#section-e087cb2e3562473e8d391abfa3b9489f}

* Om samma namn mappas till flera lager (till exempel: `layer=1,image&layer=2,image`) inträffar ett fel.
* Om samma namn mappas till ett enda lager flera gånger (till exempel: `layer=1,image&layer=1,image`), omfånget anges som vanligt, utan fel.
* Flera namn för samma lager stöds.

   Båda namnen kan användas för att referera till lagret (till exempel: `layer=1,image&layer=1,picture`).
* Om ett refererat namn aldrig mappas till ett lagernummer (till exempel: `layer=1,image&layer=picture`) inträffar ett fel.
* Ersättningsvariabler stöds inte i lagermodifierare (till exempel: `layer=$image$`).

   Detta gäller för alla permutationer, inte bara lagernamn utan för lagermodifierare i allmänhet.

* Alla regler för att sammanfoga och åsidosätta ska fungera exakt som när samma lager refereras i flera källor (begäranden, före eller efter katalogobjekt för modifiering, makron osv.).

## Exempel {#section-cc40de6a0a754178aa752601539c815b}

Se exemplen i [Mallar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
