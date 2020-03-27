---
description: Textsträngslokalisering gör att bildkataloger kan innehålla flera språkspecifika representationer för samma strängvärde.
seo-description: Textsträngslokalisering gör att bildkataloger kan innehålla flera språkspecifika representationer för samma strängvärde.
seo-title: Textsträngslokalisering
solution: Experience Manager
title: Textsträngslokalisering
topic: Scene7 Image Serving - Image Rendering API
uuid: bdff2403-e3bb-4b3f-a8d7-bb108c1fbee8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Textsträngslokalisering{#text-string-localization}

Textsträngslokalisering gör att bildkataloger kan innehålla flera språkspecifika representationer för samma strängvärde.

Servern returnerar den representation som matchar språkområdet som har angetts till klienten `locale=`och undviker därmed klientlokalisering och låter applikationerna helt enkelt växla språkområde genom att skicka lämpligt `locale=` värde med IS-textbegäranden.

## Omfång {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

Textsträngslokalisering används för alla strängelement som innehåller lokaliseringstoken ` ^loc= *`locId`*^` i följande katalogfält:

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Katalogfält</b> </th> 
   <th class="entry"> <b>Strängelement i fält</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::ImageSet </span> </p> </td> 
   <td> <p>Alla underelement som innehåller en översättningsbar sträng (avgränsas av en kombination av avgränsare ',' ';' ':' och/eller fältets start/slut). </p> <p> Ett <span class="codeph"> 0xrrggbb- </span> färgvärde i början av ett lokaliserbart fält undantas från lokalisering och skickas vidare utan ändring. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::Map </span> </p> </td> 
   <td> <p>Ett attribut med enkla eller dubbla citattecken, förutom värdena för attributen <span class="codeph"> coords= </span> och <span class="codeph"> shape= </span> . </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::mål </span> </p> </td> 
   <td> <p>Värdet för alla <span class="codeph"> mål.*.label </span> och <span class="codeph"> target.*.userdata, </span> egenskap. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::UserData </span> </p> </td> 
   <td> <p>Värdet för en egenskap. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Strängsyntax {#section-d12320edf300409f8e17565b143acafc}

Lokaliseringsaktiverade *`string`* element i bildkatalogen består av en eller flera lokaliserade strängar som föregås av en lokaliseringstoken.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span></span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span></span> </p> </td> 
  <td class="stentry"> <p>Internt språk-ID för <span class="varname"> localizedString </span> efter denna <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString </span></span> </p> </td> 
  <td class="stentry"> <p>Lokaliserad sträng. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString </span></span> </p> </td> 
  <td class="stentry"> <p>Sträng som ska användas för okända språk. </p> </td> 
 </tr> 
</table>

*`locId`* måste vara ASCII och får inte innehålla &#39;^&#39;.

&#39;^&#39; kan förekomma var som helst i delsträngar med eller utan HTTP-kodning. Servern matchar hela *`localizationToken`*`^loc=locId^` mönstret med separata delsträngar.

*`stringElements`* som inte innehåller minst en *`localizationToken`* betraktas inte som lokalisering.

## Översättningskartan {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` definierar reglerna som används av servern för att avgöra vilka som ska returneras *`localizedStrings`* till klienten. Det består av en lista med indata *`locales`* (som matchar de värden som anges med `locale=`), där vart och ett inte har något eller flera interna språk-ID ( *`locId`*). Exempel:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Tomma *`locId`* värden anger att *`defaultString`* ska returneras, om tillgängligt.

Mer information finns i beskrivningen av `attribute::LocaleStrMap` .

## Översättningsprocessen {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Med hjälp av översättningskartan ovan och begäran `/is/image/myCat/myItem?req=&locale=nl`söker servern först efter &quot; `nl`&quot; i språkområdet. Den matchade posten `nl,N` anger att för varje *`stringElement`* ska den *`localizedString`* som är markerad med `^loc=N^` returneras. Om detta inte *`localizationToken`* finns i *`stringElement`* returneras ett tomt värde.

Låt oss säga `catalog::UserData` for `myCat/myItem` innehåller följande (radbrytningar infogade för tydlighet):

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

Servern returnerar följande som svar på vår exempelbegäran:

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Okända språk {#section-26dfeefbd60345de94bbfeaaf7741223}

I ovanstående exempel `attribute::LocaleStrMap` har en post med ett tomt *`locale`* värde. Servern använder den här posten för att hantera alla `locale=` värden som inte uttryckligen anges på annat sätt i översättningskartan.

Exemplet på översättningskarta anger att i så fall ska *`defaultString`* returneras om möjligt. Följande skulle alltså returneras om översättningskartan tillämpades på begäran `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Exempel {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Språkfamiljer**

Flera *`locId`* värden kan associeras med varje *`locale`* i översättningskartan. Detta möjliggör stöd för landsspecifika eller regionspecifika varianter (t.ex. amerikansk engelska och brittisk engelska) för utvalda *`stringElements`* medan det hanterar de flesta innehåll med vanliga basspråk (t.ex. internationell engelska).

Vi vill till exempel lägga till stöd för amerikansk-specifik engelska ( ` *`locId`* EUS`) och brittisk-specifik engelska ( ` *`locId`* EUK`) som stöd för tillfällig alternativ stavning. Om EUK eller EUS inte finns, skulle vi återgå till E. På samma sätt kan österrikiska-specifika tyska varianter ( `DAT`) göras tillgängliga vid behov medan vanliga tyska återlämnas *`localizedStrings`* (markeras med `D`) under större delen av tiden.

`attribute::LocaleStrMap` ser ut så här:

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

I följande tabell beskrivs utdata för vissa representativa *`stringElement`* och *`locale`* kombinationer:

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>stringElement</i> </th> 
   <th class="entry"> <i>locale</i> </th> 
   <th class="entry"> <p>Utdatasträng </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German </span> </p> </td> 
   <td> <p> en, en_us, en_uk </p> <p> de, de_at, de_de </p> <p>alla andra </p> </td> 
   <td> <p>Engelska </p> <p>Tyska </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austria </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>alla andra </p> </td> 
   <td> <p>Engelska </p> <p>Engelska - Storbritannien </p> <p>Tyska </p> <p>Österrike </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> Observera att <span class="varname"> locId </span> DDE i det här exemplet inte finns i <span class="codeph"> -attributet::LocaleStrMap </span>, och att delsträngen som är associerad med det här <span class="varname"> locId aldrig returneras </span> . </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>alla andra </p> </td> 
   <td> <p>Engelska </p> <p>Engelska (USA) </p> <p>Tyska </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>

