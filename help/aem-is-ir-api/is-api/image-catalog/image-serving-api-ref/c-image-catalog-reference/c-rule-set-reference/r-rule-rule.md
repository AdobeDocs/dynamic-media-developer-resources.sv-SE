---
description: Regelelement för begäran. En eller flera regler är valfria i <ruleset>-elementet.
seo-description: Regelelement för begäran. En eller flera regler är valfria i <ruleset>-elementet.
seo-title: regel
solution: Experience Manager
title: regel
topic: Scene7 Image Serving - Image Rendering API
uuid: 8b8e5b06-a0b7-47e1-942d-0297d08c313b
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# regel{#rule}

Regelelement för begäran. En eller flera regler är valfria i `<ruleset>` elementet.

## Attribut {#section-d4a3b0496c0c4aa5bd7da87203b9379b}

`OnMatch = "break" | "continue" | "error"`: Valfritt. Standardvärdet är &quot;break&quot;.

`Replace = "first" | "all"`: Valfritt. Standardvärdet är &quot;first&quot;.

`RequestType` = *&quot;`types`&quot;*: Valfritt. Anger vilken indatakontext regeln gäller för. *`types`* är en kommaavgränsad lista, som kan innehålla en eller flera av de variabler som anges i följande tabell. Om `RequestType` inte anges gäller regeln för begäranden som tas emot i alla kontexter som stöds.

<table id="table_4935E1ED03624DA6AF3F8DC9AAA10237"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><b>token</b> </p> </th> 
   <th class="entry"> <p><b>Kontext</b> </p> </th> 
   <th class="entry"> <p><b>Beskrivning</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> är</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/image/</span> </p> </td> 
   <td> <p>Tillämpas på bildserverbegäranden </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ir</span> </p> </td> 
   <td> <p> <span class="filepath"> /ir/render/</span> </p> </td> 
   <td> <p>Tillämpas på begäranden om bildåtergivning </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> static</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/content/</span> </p> </td> 
   <td> <p>Tillämpas på begäranden om statiskt innehåll </p> </td> 
  </tr> 
 </tbody> 
</table>

**`Name = "text"`**: Valfritt. Används för att identifiera `<rule>` elementet i felsökningsloggar och felmeddelanden.

`  *`Attribut`* ="value"`: Valfritt. `<rule>` -element kan definiera något av följande attribut i valfri kombination. Om den anges och regeln matchas kommer de att åsidosätta motsvarande katalogattribut för den här begäran. Standardvärdet är `RequestType="is"`.

<table id="table_67AED5BEADDF4DAC99B5EF46438C1ABC"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <span class="varname"> Attribut </span></b> </th> 
   <th class="entry"> <p>Motsvarande bildkatalogsattribut </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> DefaultImageMode</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local"> attribute::DefaultImageMode</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ErrorImage</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local"> attribute::ErrorImage</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Förfaller</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7" type="reference" format="dita" scope="local"> attribute::Expiration</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> MaxPix</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local"> attribute::MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestLock</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local"> attribute::RequestLock</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestObfuscation</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local"> attribute::RequestObfuscation</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RootUrl</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local"> attribute::RootUrl</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> SavePath</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-savepath.md#reference-9c4686dc153b41d8a0751cde83615432" type="reference" format="dita" scope="local"> attribute::SavePath</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> WaterMark</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local"> attribute::WaterMark</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Mer information finns i beskrivningen av motsvarande bildkatalogsattribut.

Förfalloattributen åsidosätter bara standardattributvärdena. Åsidosättningen ignoreras om ett specifikt `catalog::Expiration` värde gäller för begäran.

## Data {#section-8fce013a4c724da58af3fee4e7a90e72}

<table id="simpletable_4F1C03671DA942A3A332B2C686A63C52"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;expression&gt;</span> </p></td> 
  <td class="stentry"> <p>Valfritt </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;ersättning&gt;</span> </p></td> 
  <td class="stentry"> <p>Valfritt </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;adressfilter&gt;</span> </p></td> 
  <td class="stentry"> <p>Valfritt </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;header&gt;</span> </p></td> 
  <td class="stentry"> <p>Valfritt </p></td> 
 </tr> 
</table>

## Anteckningar {#section-0c5fbc363070419d8c9800b0c02dc9f9}

Om både `<expression>` och `<substitution>` anges, och hämtade delsträngar inte används, ersätts den första matchande delsträngen med `<substitution>`.

Om `<expression>` inte anges matchar alla sökvägar och `<substitution>` läggs till i slutet av banan.

Om `<substitution>` inte anges sker ingen omformning av sökväg eller fråga, men alla angivna katalogattribut åsidosätts. Om `<substitution>` är tom tas den matchande delsträngen bort.

Funktionen `<addressfilter>` används bara när en matchning inträffar och innan frågeregler tillämpas.
