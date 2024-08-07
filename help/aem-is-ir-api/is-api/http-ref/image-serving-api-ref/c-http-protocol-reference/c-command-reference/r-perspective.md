---
title: perspektiv
description: Perspektivomformning. Använd en perspektivomformning på lagerkällbilden så att den fyller det område som anges med den fyrsidiga bilden. Andra områden i lagret förblir genomskinliga.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# perspektiv{#perspective}

Perspektivomformning. Använd en perspektivomformning på lagerkällbilden så att den fyller det område som anges med den fyrsidiga bilden. Andra områden i lagret förblir genomskinliga.

`perspective= *`perspQuad`*[, *`resOptions`*]`

`perspectiveN= *`perspQuadN`*[, *`resOptions`*]`

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

Modifieraren *`perspQuad`* består av fyra pixelkoordinatvärden i den sammansatta (eller lagret 0) koordinatmodellen, som utgår från det övre vänstra hörnet i den sammansatta bilden.

Modifieraren `perspQuadN` består av fyra normaliserade koordinatvärden, där `0.0,0.0` motsvarar det övre vänstra hörnet i bilden för det sammansatta lagret/lagret 0 och `1.0,1.0` mot det nedre högra hörnet.

Indatabilden omformas så att indatabildens övre vänstra hörn mappas till det första koordinatvärdet för `perspQuad[N]`, det övre högra hörnet till den andra koordinaten, det nedre högra hörnet till den tredje koordinaten och det nedre vänstra hörnet till den fjärde koordinaten.

>[!NOTE]
>
>Modifieraren `pos=` kan användas för att ytterligare placera det omformade lagret i den sammansatta bilden.

De fyra perspektivkoordinaterna kan placeras utanför den sammansatta bilden.

Beteendet är odefinierat om den kvadrilaterala inte är lämplig för en perspektivomformning. Om till exempel två eller flera hörn sammanfaller, om tre eller alla hörn finns på samma rad, eller om den fyrsidiga är självkorsande eller konkav.

## Kvalitetsaspekter {#section-7cc9056afa614300a9b8844d39739fc3}

Standardimplementeringen skapar en rimlig kompromiss mellan kvalitet och prestanda, men det kan vara nödvändigt att öka upplösningen för källbilden för att förbättra skärpan eller minska den för att minska alibreringsartefakter.

Om källan är en bild använder du `scale=` för att välja en annan upplösning (i förhållande till bildens fullständiga upplösning). Det angivna `scale=`-värdet avrundas till nästa högre PTIF-upplösningsnivå. Om det finns en kapslad begärandekälla kan storleken på bilden som skapas av den kapslade begäran justeras för att uppnå önskad skärpa. För textlager justeras upplösningen för indatabilden (den återgivna texten) genom att ett större värde = väljs och upplösningen som anges med `textAttr=` ökas.

Med modifieraren *`resOptions`* kan du välja en alternativ omsamplingsalgoritm. Följande värden stöds (skiftlägeskänsliga):

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> värde </b> </th> 
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
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> Supersampling med justerbar darr (<span class="varname"> n</span>) måste vara ett heltalsvärde mellan 0 och 200). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-818e57df0a1b4449888543bc6af77751}

kommandot Lager. Gäller det aktuella lagret eller lagret 0 om `layer=comp`. Ignoreras av effektlager.

Modifieraren `res=` ignoreras alltid när det finns perspektiv i samma lager. Modifieraren `size=` ignoreras när den anges för bildlager. Modifierarna `size=` och `res=` i lager med `perspective=` är reserverade för framtida bruk.

## Standard {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, för ingen perspektivomformning.

## Se även {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
