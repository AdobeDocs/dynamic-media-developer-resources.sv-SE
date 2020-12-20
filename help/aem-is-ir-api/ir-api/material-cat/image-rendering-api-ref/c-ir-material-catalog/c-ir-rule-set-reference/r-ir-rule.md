---
description: Regelelement för begäran. En eller flera är valfria i <ruleset>-elementet.
seo-description: Regelelement för begäran. En eller flera är valfria i <ruleset>-elementet.
seo-title: regel
solution: Experience Manager
title: regel
topic: Scene7 Image Serving - Image Rendering API
uuid: f7071681-e97e-4081-aeb1-093d2b23041c
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 1%

---


# regel{#rule}

Regelelement för begäran. En eller flera är valfria i `<ruleset>`-elementet.

## Attribut {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"` Valfritt. Standardvärdet är &quot;break&quot;.

` Name=" *``*"` textOptional. Används för att identifiera `<rule>`-elementet i felsökningsloggar och felmeddelanden.

Dessutom kan `<rule>`-element definiera följande attribut i valfri kombination. Om den anges och regeln matchas utan fel åsidosätter de motsvarande katalogattributen för den här begäran.

<table id="table_AFEFDE61C9ED40019C10D8FE5B16CA23"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>&lt;rule&gt; attribute </p> </th> 
   <th colname="col2" class="entry"> <p>Motsvarande bildkatalogsattribut </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DefaultPix  </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local"> attribute::DefaultPix  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ErrorImage  </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local"> attribute::ErrorImage  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Förfaller  </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local"> attribute::Expiration  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MaxPix  </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657" type="reference" format="dita" scope="local"> attribute::MaxPix  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RootUrl  </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402" type="reference" format="dita" scope="local"> attribute::RootUrl  </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Mer information finns i beskrivningen av motsvarande bildkatalogsattribut.

Förfalloattributet åsidosätter bara standardattributvärdet. det ignoreras om ett specifikt `catalog::Expiration`-värde gäller för begäran.

## Data {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;expression&gt; </span> </p> </td> 
  <td class="stentry"> <p>Valfritt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;substitution&gt; </span> </p> </td> 
  <td class="stentry"> <p>Valfritt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;addressfilter&gt; </span> </p> </td> 
  <td class="stentry"> <p>Valfritt. </p> </td> 
 </tr> 
</table>

## Anteckningar {#section-a27b91f9a03047c0bb7edc0967fb4216}

Om både `<expression>` och `<substitution>` anges och hämtade delsträngar inte används, ersätts den första matchande delsträngen med `<substitution>`.

Om `<expression>` inte anges matchar alla sökvägar och `<substitution>` läggs till i slutet av sökvägen.

Om `<substitution>` inte anges tas den matchande delsträngen bort.

`<addressfilter>` används bara när en matchning inträffar och innan frågeregler tillämpas.
