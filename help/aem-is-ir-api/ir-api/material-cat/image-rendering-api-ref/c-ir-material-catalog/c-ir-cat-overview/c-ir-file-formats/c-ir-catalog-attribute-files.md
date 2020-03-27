---
description: Katalogattributfiler kan ha vilket namn som helst, men måste ha ett .ini-filsuffix. De kan enkelt underhållas med valfri textredigerare.
seo-description: Katalogattributfiler kan ha vilket namn som helst, men måste ha ett .ini-filsuffix. De kan enkelt underhållas med valfri textredigerare.
seo-title: Katalogattributfiler
solution: Experience Manager
title: Katalogattributfiler
topic: Scene7 Image Serving - Image Rendering API
uuid: ea2bddad-2c4a-43c1-9b62-6e724fcfb8a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Katalogattributfiler{#catalog-attribute-files}

Katalogattributfiler kan ha vilket namn som helst, men måste ha ett .ini-filsuffix. De kan enkelt underhållas med valfri textredigerare.

Katalogattributfiler består av en uppsättning textposter, avgränsade med en enda `<CR>` (ASCII-kod 0xD), en enda `<LF>` (ASCII-kod 0xA) eller ett `<CR><LF>` par. Varje post består av ett attributnamn och ett eller flera kommaavgränsade attributvärden:

` *``*= *``*&#42;[, *`namvaluevalue`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> namn </span></span> </p> </td> 
  <td class="stentry"> <p>Attributnamn; kan bestå av en eller flera bokstäver, siffror, '-' och '_'; inte skiftlägeskänslig. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> värde </span></span> </p> </td> 
  <td class="stentry"> <p>Attributvärde; får inte innehålla <span class="codeph"> &lt;CR&gt; </span>- eller <span class="codeph"> &lt;LF&gt;- </span> tecken, såvida det inte föregås av ett omvänt snedstreck. </p> </td> 
 </tr> 
</table>

* Tomt utrymme mellan variabler är valfritt.
* Poster med okända attributnamn ignoreras av plattformsservern.
* Attributnamn kan bestå av vilken kombination som helst av ASCII-bokstäver, siffror samt &quot;-&quot;, &quot;_&quot; och &quot;.&quot;
* Om samma attributnamn förekommer mer än en gång i samma attributfil gäller det senast påträffade attributnamnet.
* Använd &#39;#&#39; som första tecken för att markera en post som en kommentar som tolkaren ignorerar.

