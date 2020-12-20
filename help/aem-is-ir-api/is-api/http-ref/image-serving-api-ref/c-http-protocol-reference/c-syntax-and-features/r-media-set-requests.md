---
description: Image Serving är en mekanism för att hämta ett hierarkiskt textsvar (xml eller json) som representerar alla resurser och metadata som är associerade med en katalog ImageSet för en viss post.
seo-description: Image Serving är en mekanism för att hämta ett hierarkiskt textsvar (xml eller json) som representerar alla resurser och metadata som är associerade med en katalog ImageSet för en viss post.
seo-title: Medieuppsättningsbegäranden
solution: Experience Manager
title: Medieuppsättningsbegäranden
topic: Scene7 Image Serving - Image Rendering API
uuid: af9fabcd-531d-43fb-bd97-269923bea5e8
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '995'
ht-degree: 0%

---


# Medieuppsättningsbegäranden{#media-set-requests}

Image Serving är ett sätt att hämta ett hierarkiskt textsvar (xml eller json) som representerar alla resurser och metadata som är associerade med katalogen::ImageSet för en viss post.

Visningsprogrammen kan använda den här funktionen för att generera svar som informerar presentationen av enkla bilder, videoklipp, videouppsättningar, färgruteuppsättningar, siduppsättningar (e-kataloger) och mediauppsättningar.

## Syntax för begäran {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

Du kan hämta det angivna svaret för en `catalog::ImageSet` med modifieraren `req=set` och referera till katalogpost-ID:t i nätsökvägen. Alternativt kan bilduppsättningen anges direkt i URL-adressen med modifieraren `imageset=`. Om modifieraren `imageset=` används för att ange bilduppsättningen bör hela värdet omges av klammerparenteser för att undvika bilduppsättningsvärdet och för att säkerställa att alla inkluderade modifierare inte tolkas som en del av URL-frågesträngen.

## Typer av inställda svar {#section-93eb0a1f70344da2a888e56372ad3896}

Mekanismen set har stöd för följande typer av svar:

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>enkla bilder </p></td> 
  <td class="stentry"> <p>En bildpost utan <span class="codeph">-katalog::ImageSet</span> definierad. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>enkla videoklipp </p></td> 
  <td class="stentry"> <p>En videopost i den statiska innehållskatalogen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>färgruteuppsättningar </p></td> 
  <td class="stentry"> <p>En uppsättning objekt som består av en referens till en bildpost och en valfri separat referens till en bildpost som används som en färgruta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>hierarkiska färgruteuppsättningar </p></td> 
  <td class="stentry"> <p>En uppsättning objekt som består av ett grundläggande färgruteobjekt eller en referens till en post för färgruteuppsättning. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>snurra uppsättningar </p></td> 
  <td class="stentry"> <p>En uppsättning objekt som består av en enkel lista med bild-ID:n. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>tvådimensionella snurruppsättningar </p></td> 
  <td class="stentry"> <p>En uppsättning med objekt som består av en enkel bild eller en referens till en grundläggande snurruppsättning. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>siduppsättningar </p></td> 
  <td class="stentry"> <p>En uppsättning objekt som består av en lista med upp till tre sidbilder </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>medieuppsättningar </p></td> 
  <td class="stentry"> <p>En uppsättning objekt som består av enkla bilder, videouppsättningar, färgruteuppsättningar, hierarkiska färgruteuppsättningar, snurruppsättningar, tvådimensionella snurruppsättningar, siduppsättningar och videoresurser. Varje medieuppsättningsobjekt kan också innehålla en valfri färgruta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>videouppsättningar </p></td> 
  <td class="stentry"> <p>En uppsättning med objekt som består av en lista med enkla videoklipp. </p></td> 
 </tr> 
</table>

## Identifiering av typ för yttre uppsättning {#section-3dd6e453528d46898e559d31458a59ba}

När en `req=set`-begäran tas emot bestäms vilken typ av svar som ska genereras av värdet `catalog::AssetType`. Om `catalog::AssetType` inte är definierad bestäms svarstypen av följande regler:

* Om en post hittas i bildkatalogen definieras AND `catalog::ImageSet`

   * Anta att e-katalog har angetts om minst en post i fältet Imageset innehåller ett kolon
   * Anta att medieuppsättningar finns om minst en post i fältet Imageset innehåller två semikolon.
   * Anta att bilduppsättningen är om minst en post i fältet Imageset innehåller ett semikolon.
   * Anta att snurra anges om ingen post innehåller kolon eller semikolon, men minst en post innehåller en referensuppsättning eller en intern uppsättning (detta är en 2D-snursuppsättning).
   * Anta att en okänd uppsättning saknas om det inte finns någon post som innehåller kolon eller semikolon eller refererad uppsättning eller textbunden uppsättning (t.ex. en kommaseparerad lista med bilder).

* Om post hittas i både bild OCH statiska innehållskataloger

   * Anta video om filtillägget finns i följande uppsättning: mp3, mp4, flv, f4v, swf, xml
   * Anta annars att bilden

* Om en post hittas i en statisk innehållskatalog men INTE i bildkatalogen

   * Anta video om filtillägget finns i följande uppsättning: mp3, mp4, flv, f4v, swf, xml
   * Anta statiskt annars

* Om en post hittades i bildkatalogen men INTE i den statiska innehållskatalogen

   * Anta bild

* Om posten INTE hittas i bildkatalogen och INTE hittas i den statiska innehållskatalogen

   * Anta filbaserad video om filtillägget finns i följande uppsättning: mp3, mp4, flv, f4v, swf, xml
   * Anta annars filbaserad bild

I samtliga fall kommer det resulterande xml-svaret att överensstämma med det angivna XML-dokumentet med den angivna rotnoden som motsvarar den identifierade typen.

## Identifiering av intern typ {#section-8f46490e467247e69ce284704def06f3}

När den yttre uppsättningen identifieras som en typ av medieuppsättning innehåller svaret en uppsättning medieuppsättningsobjekt som motsvarar varje medieuppsättningspost i `catalog::ImageSet`. Om den valfria typparametern anges för en viss medieuppsättningspost mappas den till en utdatatyp enligt följande tabell:

| Indatatyp | Utdatatyp |
|---|---|
| `img` | `img` |
| `basic` | `img` |
| `advanced_image` | `img` |
| `img_set` | `img_set` |
| `advanced_image_set` | `img_set` |
| `advanced_swatchset` | `img_set` |
| `spin` | `spin` |
| `video` | `video` |
| `video_set` | `video_set` |
| `static` | `static` |
| `ecat` | `ecat` |

Om den valfria typparametern för en viss medieuppsättningspost inte har angetts eller motsvarar en typ som inte stöds, identifieras medieuppsättningens objekttyp automatiskt med samma regler som tillämpades på den yttre uppsättningsnivån.

## XML-specifikation {#section-c1bd60948ef545759a16885bb6fcc607}

Det returnerade xml-svaret uppfyller följande specifikation:

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

Modifieraren `labelkey=` används tillsammans med fältet `catalog::UserData`för att generera etiketter för bilder och färgrutor. Fältet `catalog:UserData` tolkas som en uppsättning nyckel/värde-par och etikettnyckelindexen i den här uppsättningen för att hämta värdet för den angivna nyckeln. Värdet returneras sedan i attributet *`l`* för *`s`* och *`i`*.

## Tvingande begränsningar {#section-b9f042873bee45a5ae11b69fd42f2bca}

För att begränsa svarsstorleken och förhindra självrefererande problem, styrs det maximala kapslingsdjupet av serveregenskapen `PS::fvctx.nestingLimit`. Om gränsen överskrids returneras ett fel.

För att begränsa storleken på xml-svaren för stora e-kataloguppsättningar, inaktiveras privata metadata för broschyruppsättningsobjekt enligt serveregenskapen `PS::fvctx.brochureLimit`. Alla privata metadata som är associerade med broschyren exporteras tills broschyrgränsen nås. När gränsen har överskridits ignoreras privata kartor och användardata och en motsvarande flagga ställs in för att ange vilken typ av data som har utelämnats.

Kapslade medieuppsättningar stöds inte. En kapslad medieuppsättning definieras som en medieuppsättning som innehåller en medieuppsättning av medietyp. Om det här tillståndet upptäcks returneras ett fel.

## Exempel {#section-588c9d33aa05482c86cd2b1936887228}

XML-svar för `req=set`-begäran finns på sidan Egenskaper under rubriken HTML-exempel.

`http://crc.scene7.com/is-docs/examples/properties.htm`

## Se även {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3),  [katalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md),  [Image Catalog Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)

