---
description: Image Serving är en mekanism som översätter externa objekt-ID:n till språkområdesspecifika objekt-ID:n (katalog). Det primära programmet är att tillhandahålla språkområdesspecifikt innehåll och innehåll som delas mellan flera språkområden utan att klientprogrammet behöver känna till de språkområdesspecifika objekt-ID:n.
seo-description: Image Serving är en mekanism som översätter externa objekt-ID:n till språkområdesspecifika objekt-ID:n (katalog). Det primära programmet är att tillhandahålla språkområdesspecifikt innehåll och innehåll som delas mellan flera språkområden utan att klientprogrammet behöver känna till de språkområdesspecifika objekt-ID:n.
seo-title: Översättning av objekt-ID
solution: Experience Manager
title: Översättning av objekt-ID
topic: Scene7 Image Serving - Image Rendering API
uuid: 8b4c2f44-033a-428a-b505-af389865c70a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Översättning av objekt-ID{#object-id-translation}

Image Serving är en mekanism som översätter externa objekt-ID:n till språkområdesspecifika objekt-ID:n (katalog). Det primära programmet är att tillhandahålla språkområdesspecifikt innehåll och innehåll som delas mellan flera språkområden utan att klientprogrammet behöver känna till de språkområdesspecifika objekt-ID:n.

Programmet kan bara skrivas med globala objekt-ID:n, och i stället för språkspecifika bilder och annat innehåll ersätts automatiskt vid behov.

Detta *`locale`* anges i Image Serving-begäranden med `locale=` kommandot.

>[!NOTE]
>
>Översättning av objekt-ID gäller endast för katalogbaserad användning av bildservering. Det går inte att översätta filnamn.

## Omfång {#section-66fcd5bd467c4eeaa1574583cbe9756d}

Alla referenser till poster i bildkataloger, SVG-filer och statiska innehållskataloger beaktas för översättningsteckensnitt och ICC-profilreferenser översätts inte. Förutom sökvägen *`object`* till [!DNL /is/image] och [!DNL /is/static requests]är dessa kommandon och katalogattribut föremål för ID-översättning: `src=`, `mask=`, `template=`, `defaultImage=`, `attribute::DefaultImage`och `attribute::Watermark`.

## Översättningskarta för ID {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` definierar reglerna som används av servern för att fastställa ID:t för det lokaliserade innehållet, givet som indata till det generiska objektet ID och `locale=` värdet.

`attribute::LocaleMap` består av en lista med *inmatningsspråk* (som matchar de värden som anges med `locale=`), där vart och ett saknar eller har utmatningssuffix ( ` *`locSuffixes`*`).

Så `attribute::LocaleMap` här ser till exempel ut:

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

Begäran `/is/image/myCat/myImg?locale=de_de` returnerar den bild som är associerad med katalogposten `myCat/myImg_D` (förutsatt att det finns en sådan katalogpost).

Mer information finns i beskrivningen av `attribute::LocaleMap` .

## Översättningsprocessen {#section-1f64db17e9f644d88e09853670e14a16}

Med hjälp av exemplet ovan söker servern först efter *`locale`* &quot; `de_de`&quot; i ID-översättningskartan. Sedan itereras den över *`locSuffixes`* som är associerad med den här posten, i det här fallet &quot; `_D`&quot; och &quot;&quot; (tomt suffix). För varje upprepning läggs suffixet till bild-ID:t och det resulterande ID:t som testas finns i katalogen. Om det hittas används katalogposten, annars testas nästa. I det här exemplet kontrolleras följande poster: `myCat/myImg_D`, och `myCat/myImg`. Om ingen matchning hittas returnerar servern ett fel eller en standardbild (om den är konfigurerad).

## Okända språk {#section-b2f3c83f2dc845d69b5908107b775537}

I ovanstående exempel `attribute::LocaleMap` innehåller en tom *`locale`* som definierar standardöversättningsregeln, som används för okända `locale=` värden (dvs. de som inte uttryckligen anges i översättningsschemat). Om den här översättningskartan tillämpades på begäran `/is/image/myCat/myImg?locale=ja`skulle den matchas till `myCat/myImg_E`, om den finns, eller på annat sätt `myCat/myImg`.

Om en översättningskarta inte anger någon standardöversättningsregel returneras ett fel för alla begäranden med okända `locale=` värden.

## Exempel {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**Uppslag på flera nivåer**

Det är ofta önskvärt att gruppera språkområden (till exempel europeiska, Mellanöstern och Nordamerika) för att ta hänsyn till regionala standarder. Detta kan uppnås med en sökning på flera nivåer.

I det här exemplet vill vi stödja samlingar för väst- och Mellanöstern-användning. Båda samlingarna är baserade på den generiska bildsamlingen, och båda lägger till eller ändrar vissa bilder. Båda samlingarna förfinas sedan ytterligare för specifika språkområden ( `m1`, `m2` för två varianter från Mellanöstern och `w1`, `w2`och `w3` för tre västerländska språkområden), förutom att bilder delas för `w1` och `w3`. Okända språk mappas endast till den generiska samlingen och har inte tillgång till språkspecifika bilder.

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

I följande tabell visas vilka kataloginlägg som kommer att övervägas och i vilken ordning de kommer att övervägas för det generiska indata-ID:t `myImg`:

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>språkinställning</i></b> </th> 
   <th class="entry"> <b>Katalog-ID:n som ska genomsökas</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1, w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2, myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>alla andra </p> </td> 
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Sök efter specifika ID:n**

Vissa namngivningskonventioner kanske inte stöder generiska bild-ID internt. De generiska ID:n från begäran måste alltid mappas till ett specifikt ID i katalogen. ofta är det inte säkert att det exakta specifika ID:t är känt.

I det här exemplet kan bilder för alla språk ha `_1`, `_2`eller suffix `_3` . Bilder som är specifika för franska språkområden kan ha `_22` - eller `_23` suffix, och bilder som är specifika för tyska språkområden kan ha `_470` - eller `_480` suffix.

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

I följande tabell visas vilka katalogposter som beaktas och i vilken ordning de betraktas som ett allmänt indata-ID `myImg`:

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>språkinställning</i></b> </th> 
   <th class="entry"> <b>Utdata-ID som ska genomsökas</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>, <span class="codeph"> de_at </span>, <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>alla andra </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Se även {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) , [attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b), [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
