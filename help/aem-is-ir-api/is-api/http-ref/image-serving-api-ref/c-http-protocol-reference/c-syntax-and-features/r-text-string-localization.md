---
description: Textsträngslokalisering gör att bildkataloger kan innehålla flera språkspecifika representationer för samma strängvärde.
solution: Experience Manager
title: Textsträngslokalisering
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 0%

---

# Textsträngslokalisering{#text-string-localization}

Textsträngslokalisering gör att bildkataloger kan innehålla flera språkspecifika representationer för samma strängvärde.

Servern returnerar till klienten den representation som matchar det språk som har angetts med `locale=`och därmed undvika lokalisering på klientsidan och låta applikationerna helt enkelt byta språkområde genom att skicka lämpliga `locale=` med IS-textbegäranden.

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
   <td> <p>Alla underelement som innehåller en översättningsbar sträng (avgränsas av en kombination av avgränsare ',' ';' ':' och/eller fältets start/slut). </p> <p> A <span class="codeph"> 0xrrggbb </span> färgvärdet i början av ett lokaliserbart fält är exkluderat från lokaliseringen och skickas vidare utan ändring. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::Map </span> </p> </td> 
   <td> <p>Ett attributvärde med enkla eller dubbla citattecken, förutom värdena för <span class="codeph"> coords= </span> och <span class="codeph"> shape= </span> attribut. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::mål </span> </p> </td> 
   <td> <p>Värdet för <span class="codeph"> mål.*.label </span> och <span class="codeph"> mål.*.userdata </span> -egenskap. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> katalog::UserData </span> </p> </td> 
   <td> <p>Värdet för en egenskap. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Strängsyntax {#section-d12320edf300409f8e17565b143acafc}

Lokalisering är aktiverat *`string`* -element i bildkatalogen består av en eller flera lokaliserade strängar, som föregås av en lokaliseringstoken.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>Internt språk-ID för <span class="varname"> localizedString </span> följer detta <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString </span> </span> </p> </td> 
  <td class="stentry"> <p>Lokaliserad sträng. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString </span> </span> </p> </td> 
  <td class="stentry"> <p>Sträng som ska användas för okända språk. </p> </td> 
 </tr> 
</table>

*`locId`* måste vara ASCII och får inte innehålla &#39;^&#39;.

&#39;^&#39; kan förekomma var som helst i delsträngar med eller utan HTTP-kodning. Servern matchar hela *`localizationToken`* `^loc=locId^` mönster för att separera delsträngar.

*`stringElements`* som inte innehåller minst en *`localizationToken`* inte används för lokalisering.

## Översättningskartan {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` definierar reglerna som används av servern för att avgöra vilka *`localizedStrings`* för att gå tillbaka till klienten. Den består av en lista med indata *`locales`* (matchar de värden som anges med `locale=`), vart och ett med inget eller flera interna språk-ID ( *`locId`*). Till exempel:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Tom *`locId`* värden anger att *`defaultString`* returneras om möjligt.

Se beskrivningen av `attribute::LocaleStrMap` för mer information.

## Översättningsprocessen {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Utifrån översättningskartan ovan och begäran `/is/image/myCat/myItem?req=&locale=nl`, söker servern först efter &quot; `nl`&quot; på språkinställningskartan. Den matchade posten `nl,N` visar att för varje *`stringElement`*, *`localizedString`* markerad med `^loc=N^` ska returneras. Om detta *`localizationToken`* finns inte i *`stringElement`*, returneras ett tomt värde.

Låt oss säga `catalog::UserData` for `myCat/myItem` innehåller följande (radbrytningar infogade för tydlighet):

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

Servern returnerar följande som svar på vår exempelbegäran:

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Okända språk {#section-26dfeefbd60345de94bbfeaaf7741223}

I exemplet ovan `attribute::LocaleStrMap` har en post med en tom *`locale`* värde. Servern använder den här posten för att hantera alla `locale=` värden som inte uttryckligen anges på annat sätt i översättningskartan.

Exempelöversättningskartan anger att i så fall *`defaultString`* returneras om möjligt. Följande skulle alltså returneras om översättningskartan tillämpades på begäran `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Exempel {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Språkfamiljer**

Flera *`locId`* värden kan associeras med varje *`locale`* i översättningskartan. Detta möjliggör stöd för landsspecifika eller regionspecifika variationer (t.ex. amerikansk engelska jämfört med brittisk engelska) för utvalda *`stringElements`* vid hantering av det mesta innehållet med vanliga basspråk (t.ex. internationell engelska).

Vi vill till exempel lägga till stöd för amerikansk-specifik engelska ( `*`locId`* EUS`) och brittisk-specifik engelska ( `*`locId`* EUK`) för att stödja tillfällig alternativ stavning. Om EUK eller EUS inte finns, skulle vi återgå till E. På samma sätt, österrikiska-specifika tyska varianter ( `DAT`) skulle kunna göras tillgänglig där det behövs medan man återgår till Tyskland *`localizedStrings`* (markerat med `D`) oftast.

`attribute::LocaleStrMap` ser ut så här:

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

Följande tabell beskriver utdata för en viss representant *`stringElement`* och *`locale`* kombinationer:

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
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> Observera att i det här exemplet är <span class="varname"> locId </span> DDE finns inte i <span class="codeph"> attribute::LocaleStrMap </span>och därmed den delsträng som är kopplad till detta <span class="varname"> locId </span> får aldrig tillbaka. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>alla andra </p> </td> 
   <td> <p>Engelska </p> <p>Engelska (USA) </p> <p>Tyska </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
