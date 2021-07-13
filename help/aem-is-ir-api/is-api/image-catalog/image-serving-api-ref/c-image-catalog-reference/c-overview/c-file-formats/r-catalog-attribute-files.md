---
description: Katalogattributfiler kan ha vilket namn som helst, men måste ha ett .ini-filsuffix. De kan enkelt underhållas med valfri textredigerare.
solution: Experience Manager
title: Katalogattributfiler
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Katalogattributfiler{#catalog-attribute-files}

Katalogattributfiler kan ha vilket namn som helst, men måste ha ett .ini-filsuffix. De kan enkelt underhållas med valfri textredigerare.

Katalogattributfiler består av en uppsättning textposter, avgränsade med en `<CR>` (ASCII-kod `0xD`), en enskild `<LF>` (ASCII-kod `0xA`) eller ett `<CR><LF>`-par. Varje post består av ett attributnamn och ett eller flera kommaavgränsade attributvärden:

`*``*= *`namvalues`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> values</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> värden</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>Attributnamn. Kan bestå av en eller flera bokstäver, siffror, - och _. Inte skiftlägeskänsligt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Attributvärde. Får inte innehålla <span class="codeph"> &lt;CR&gt;</span> eller <span class="codeph"> &lt;LF&gt;</span> tecken, såvida det inte föregås av ett omvänt snedstreck. </p></td> 
 </tr> 
</table>

Tomt utrymme mellan variabler är valfritt.

Poster med okända attributnamn ignoreras av plattformsservern.

Attributnamn kan bestå av vilken kombination som helst av ASCII-bokstäver, siffror samt &quot;-&quot;, &quot;_&quot; och &quot;.&quot;.

Om samma attributnamn förekommer mer än en gång i samma attributfil gäller det senast påträffade attributnamnet.

Använd # som det första tecknet för att markera en post som en kommentar, som tolkas som en kommentar.
