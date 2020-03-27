---
description: Använd de här serverinställningarna för att logga åtkomst.
seo-description: Använd de här serverinställningarna för att logga åtkomst.
seo-title: Åtkomstloggning
solution: Experience Manager
title: Åtkomstloggning
topic: Scene7 Image Serving - Image Rendering API
uuid: ea7d5d39-3f0a-45f0-bc28-6828a9c9da50
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Åtkomstloggning{#access-logging}

Använd de här serverinställningarna för att logga åtkomst.

Syntax

## TC::directory - loggfilsmapp {#section-5d9e2168d4504bbe9868b7d6051c9d67}

Mappen som plattformsservern skriver loggfiler till. Detta kan vara en absolut sökväg eller en relativ sökväg *`install_folder`*. Standardvärdet är [!DNL  *`install_folder`*/loggar].

>[!NOTE]
>
>Den nya mappen måste skapas innan den här inställningen ändras. Kontrollera att mappen har rätt läs-/skrivbehörighet om Image Serving är installerat för att köras under ett annat användarkonto än root.

## TC::maxDays - Antal dagar som loggfiler ska sparas {#section-45cbecffc5694c87b7d5c176a44a4885}

Antalet dagar som loggfiler ska bevaras. Nya loggfiler skapas varje dag vid midnatt. Nu tar servern bort alla filer i loggfilsmappen som är äldre än det angivna antalet dagar, inklusive de som skrivits av Image Server eller Render Server. Standardvärdet är 10.

## TC::prefix - Access Log File Name {#section-1003856323b844049632710a5a056aa7}

Namnprefix för filen som åtkomstloggdata skrivs till. Datumet och filsuffixet ( [!DNL  *`yyyy`*- *`mm`*- *`dd`*.log]) läggs till i den angivna strängen. Namnet på åtkomstloggfilen måste vara ett annat än namnet på spårningsloggfilen. Standardvärdet är &quot; `access-`&quot;.

## TC::pattern - Access Log Pattern {#section-22775ea85cee444d8a7d7336a3b1feef}

Anger datamönstret för loggposter för åtkomst till plattformsservern. Mönstersträngen anger variabler som ersätts med motsvarande värden. Alla andra tecken i mönstersträngen överförs bokstavligen till loggposten.

Om du vill använda cacheuppvärmningsverktyget måste blanksteg användas som fältavgränsare. Plattformsservern ersätter alla blanksteg och %-tecken i fältvärden med `%20` respektive `%25`.

Följande mönstervariabler stöds:

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Mönster</b> </th> 
   <th class="entry"> <b>Beskrivning</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> %a </span> </p> </td> 
   <td> <p>Fjärr-IP-adress. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %A </span> </p> </td> 
   <td> <p>Lokal IP-adress. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %b </span> </p> </td> 
   <td> <p>Antal byte för svar exklusive HTTP-huvuden, eller om noll. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>Antal byte för svar exklusive HTTP-huvuden. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>Begär bearbetningstid i millisekunder. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>tread-id (för korsrefererande felsöknings-/felloggsposter). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>datum och tid, formaterat som <span class="codeph"> <span class="varname"> yyyy </span>- <span class="varname"> MM </span>- <span class="varname"> dd </span><span class="varname"> HH </span>: <span class="varname"> mm </span>: <span class="varname"> ss </span>. <span class="varname"> SSS- </span> förskjutning </span> </p> <p> ( <span class="varname"> SSS </span> är msek, förskjutning <span class="varname"> </span> är GMT-tidsförskjutning), tidsvärdet hämtas när svaret skickas till klienten. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>Begärandemetod ( <span class="codeph"> GET </span>, <span class="codeph"> POST </span>o.s.v.). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>Begärandeöverlappning (antal begäranden som behandlas samtidigt). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>Lokal port som den här begäran togs emot på. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>Frågesträng (med "?" som prepensation) om det finns). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>Första raden i begäran (begärandemetod, URI, HTTP-version). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p>Samma som <span class="codeph"> %r </span>men tillämpar begränsad HTTP-kodning på URI för att undvika problem med loggparsning. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>Statuskod för HTTP-svar. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>Användarsessions-ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>Datum och tid, i gemensamt loggformat. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>Fjärranvändare som autentiserades (om det fanns någon), else ''. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U </span> </p> </td> 
   <td> <p>URI-sökväg. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v </span> </p> </td> 
   <td> <p>Lokalt servernamn. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T </span> </p> </td> 
   <td> <p>Begär bearbetningstid i sekunder. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r </span> </p> </td> 
   <td> <p>Plattformsserverns cachenyckel (cachefilens mapp/namn). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r </span> </p> </td> 
   <td> <p>Nyckelord för hantering av plattformsservercache: <span class="codeph"> { ÅTERANVÄND| SKAPAD| UPPDATERAD| FJÄRRANSLUTNING| REMOTE_CREATED| REMOTE_UPDATED| REMOTE_CACHE| VALIDERAD| IGNORERAD| UNDEFINED } </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r </span> </p> </td> 
   <td> <p>MIME-typ för svar. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>Målkontexten om en kontext framåt inträffar. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r </span> </p> </td> 
   <td> <p>Värdet för <span class="codeph"> taggens </span> svarshuvud (MD5-signatur för svarsdata). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r </span> </p> </td> 
   <td> <p>Felmeddelande. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r </span> </p> </td> 
   <td> <p>Tidsåtgång för att hämta cachepost eller data från Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r </span> </p> </td> 
   <td> <p>Tid för begärandetolkning och bildkatalogsökning. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r </span> </p> </td> 
   <td> <p>Anger om den här begäran försökte utföra någon sökvägsbaserad åtkomst utanför katalogsystemet. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r </span> </p> </td> 
   <td> <p>IP-adressen till den peer-server i cacheklustret som levererade cacheposten eller '-' om <span class="codeph"> CacheUse </span> varken är <span class="codeph"> REMOTE_CREATED </span> eller <span class="codeph"> REMOTE_UPDATED </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r </span> </p> </td> 
   <td> <p>Felkategori: </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=inget fel. </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=bild(er) hittades inte på servern. </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=IS-protokollanvändningsfel eller ett annat innehållsfel än 1. </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=annat serverfel. </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=begäran nekades på grund av tillfällig serveröverbelastning. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r </span> </p> </td> 
   <td> <p>Det övre värdet för <span class="codeph"> req= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r </span> </p> </td> 
   <td> <p>rotations-ID för begärans huvudkatalog. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r </span> </p> </td> 
   <td> <p>Den tid det tar för Platform Server att skicka svar efter att data har skrivits till utdataströmmen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r </span> </p> </td> 
   <td> <p>Som <span class="codeph"> %B </span>men innehåller värden för 304 (inte ändrade) svar. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformedUrl}r </span> </p> </td> 
   <td> <p>Den slutliga URL:en efter alla omformningar av regeluppsättningar. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpRequestHeader </span>}i </span> </p> </td> 
   <td> <p>Värdet för den angivna HTTP-begärandehuvudet. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpResponseHeader </span>} </span> </p> </td> 
   <td> <p>Värdet för den angivna HTTP-svarshuvudet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Standard är `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
