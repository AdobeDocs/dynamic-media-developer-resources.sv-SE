---
description: Perspektivomformning. Använd en perspektivomformning på lagerkällbilden för att fylla det område som anges med den fyrsidiga bilden. Andra områden i lagret förblir genomskinliga.
seo-description: Perspektivomformning. Använd en perspektivomformning på lagerkällbilden för att fylla det område som anges med den fyrsidiga bilden. Andra områden i lagret förblir genomskinliga.
seo-title: perspektiv
solution: Experience Manager
title: perspektiv
topic: Scene7 Image Serving - Image Rendering API
uuid: b22d7b49-db08-48df-80bc-5b7237aea475
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---


# perspektiv{#perspective}

Perspektivomformning. Använd en perspektivomformning på lagerkällbilden för att fylla det område som anges med den fyrsidiga bilden. Andra områden i lagret förblir genomskinliga.

`perspective= *``*[, *`perspQuadresOptions`*]`

`perspectiveN= *``*[, *`perspQuadNresOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>Perspektivfyrsidiga pixelkoordinater (8 realer, avgränsade med kommatecken). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>Perspektivfyrsidiga normaliserade koordinater (8 realer, avgränsade med kommatecken). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>Omsamplingsalternativ (se nedan). </p></td> 
 </tr> 
</table>

*`perspQuad`* består av fyra pixelkoordinatvärden i den sammansatta (eller lager 0) koordinatmodellen, som kommer från det övre vänstra hörnet i den sammansatta bilden.

`perspQuadN` består av fyra normaliserade koordinatvärden, där  `0.0,0.0` motsvarar det övre vänstra hörnet av bilden för det sammansatta lagret/lagret 0 och  `1.0,1.0` det nedre högra hörnet.

Indatabilden omformas så att indatabildens övre vänstra hörn mappas till det första koordinatvärdet `perspQuad[N]`, det övre högra hörnet till den andra koordinaten, det nedre högra hörnet till den tredje koordinaten och det nedre vänstra hörnet till den fjärde koordinaten.

>[!NOTE]
>
>`pos=` kan användas för att ytterligare placera det omformade lagret i den sammansatta bilden.

De fyra perspektivkoordinaterna kan placeras utanför den sammansatta bilden.

Beteendet är odefinierat om den kvadrilaterala formen inte är lämplig för en perspektivomformning (t.ex. om två eller flera hörn sammanfaller, om tre eller alla hörn är på samma linje eller om den kvadrilaterala är självkorsande eller konkav).

## Kvalitetsaspekter {#section-7cc9056afa614300a9b8844d39739fc3}

Standardimplementeringen skapar en rimlig kompromiss mellan kvalitet och prestanda, men ibland kan det vara nödvändigt att öka upplösningen för källbilden för att förbättra skärpan eller minska den för att minska aliaseringsartefakter.

Om källan är en bild använder du `scale=` för att välja en annan upplösning (i förhållande till bildens fullständiga upplösning). Det angivna `scale=`-värdet avrundas till nästa högre PTIF-upplösningsnivå. Om det gäller en kapslad begärankälla kan storleken på bilden som skapas av den kapslade begäran justeras för att uppnå önskad skärpa. För textlager justeras upplösningen för indatabilden (den återgivna texten) genom att ett större värde än= väljs samtidigt som upplösningen som anges med `textAttr=` ökas.

*`resOptions`* gör att du kan välja en alternativ omsamplingsalgoritm. Följande värden stöds (skiftlägeskänsliga):

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Värde</b> </th> 
   <th class="entry"> <b> Beskrivning</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> R1</span> </p> </td> 
   <td> <p> Närmaste granne. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> Dubbellinjär. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> Standardsupersampling (standard). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3<span class="varname"> Tn</span></span> </p> </td> 
   <td> <p> Supersampling med justerbar darr (<span class="varname"> n</span> måste vara ett heltalsvärde mellan 0 och 200). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-818e57df0a1b4449888543bc6af77751}

Lager, kommando. Gäller för det aktuella lagret eller för lagret 0 om `layer=comp`. Ignoreras av effektlager.

`res=` ignoreras alltid när det finns perspektiv i samma lager. `size=` ignoreras när det anges för bildlager. `size=` och  `res=` i lager med  `perspective=` är reserverade för framtida bruk.

## Standard {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, utan perspektivomformning.

## Se även {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) ,  [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065),  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
