---
description: Grundsyntaxen för HTTP-protokollet är följande.
seo-description: Grundsyntaxen för HTTP-protokollet är följande.
seo-title: Grundläggande syntax för Image Serving HTTP-protokoll
solution: Experience Manager
title: Grundläggande syntax för Image Serving HTTP-protokoll
topic: Scene7 Image Serving - Image Rendering API
uuid: 3269c2f2-df0f-4b62-ae9c-a267acae8071
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Grundläggande syntax för Image Serving HTTP-protokoll{#image-serving-http-protocol-basic-syntax}

Grundsyntaxen för HTTP-protokollet är följande.

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> begäran</span></span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][?<span class="varname"> modifierare</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> server </span></span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> port</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> objekt</span></span> </p></td> 
  <td class="stentry"> <p>Källobjektsspecificerare (bildsökväg eller bildkatalogpost). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifierare</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifier</span>*[&amp;<span class="varname"> modifier</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifierare</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">kommando|{$<span class="varname"> macro</span>$}|{.<span class="varname"> kommentar</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> kommando</span></span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}}[=<span class="varname"> värde</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> makro</span></span> </p> </td> 
  <td class="stentry"> <p>Namnet på ett kommandomakro. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> kommentar</span></span> </p></td> 
  <td class="stentry"> <p>Kommentarssträng (ignoreras av servern). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span></span> </p></td> 
  <td class="stentry"> <p>Ett av de kommandon eller attributnamn som stöds. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span></span> </p> </td> 
  <td class="stentry"> <p>Namnet på en anpassad variabel. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> värde</span></span> </p></td> 
  <td class="stentry"> <p>Kommando eller variabelvärde. </p></td> 
 </tr> 
</table>

*`server_address`*, *`cmdName`*, *`macro`* och *`var`* är inte skiftlägeskänsliga. Servern bevarar skiftläget för alla andra strängvärden.

*`value`* är kommandospecifikt och kan bestå av ett eller flera värden avgränsade med kommatecken. Mer information finns i beskrivningen av de enskilda kommandona.

## Server-ID {#section-926ae55ddba14b8d952147a5fd701e14}

Rotkontexten krävs för alla HTTP-begäranden till bildservern. [!DNL /is/image]

## HTTP-avkodning {#section-20922baccd804d2d986b44ce9a183a7d}

Image Serving först extraherar *`object`* och *`modifiers`* från den inkommande begäran. *`object`* separeras sedan till sökvägselement som är individuellt HTTP-avkodade. Strängen separeras till *`modifiers`* = *`command`* par och *`value`* *`value`* HTTP-avkodas sedan före kommandospecifik bearbetning.

>[!NOTE]
>
>Om inget annat anges i dokumentationen måste alla osäkra tecken kodas enligt HTTP-standarden. Mer information finns i HTTP-specifikationen.

## Kommentarer {#section-69ef0be0f17a418c87a0eba21c2ddb00}

Kommentarer kan bäddas in i begärandesträngar var som helst och identifieras av en punkt (.) direkt efter kommandoavgränsaren (&amp;). Kommentaren avslutas av nästa förekomst av en (okodad) kommandoavgränsare. Den här funktionen kan användas för att lägga till information i begäran som inte är avsedd för Image Serving, t.ex. tidsstämplar, databas-ID:n etc.

## Se även {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[Datatyper](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa), [HTTP/1.1-specifikation](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
