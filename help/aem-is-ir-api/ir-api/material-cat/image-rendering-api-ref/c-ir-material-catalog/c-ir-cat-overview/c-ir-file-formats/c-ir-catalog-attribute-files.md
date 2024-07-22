---
title: Katalogattributfiler
description: Katalogattributfiler kan ha vilket namn som helst, men måste ha ett .ini-filsuffix. De kan enkelt underhållas med valfri textredigerare.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Katalogattributfiler{#catalog-attribute-files}

Katalogattributfiler kan ha vilket namn som helst, men måste ha filsuffixet `.ini`. De kan enkelt underhållas med valfri textredigerare.

Katalogattributfiler består av en uppsättning textposter, avgränsade med en `<CR>` (ASCII-kod 0xD), en enskild `<LF>` (ASCII-kod 0xA) eller ett `<CR><LF>` -par. Varje post består av ett attributnamn och ett eller flera kommaavgränsade attributvärden:

`*`name`*= *`value`*&#42;[, *`value`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Attributnamn; kan bestå av en eller flera bokstäver, siffror, - (bindestreck) och _ (understreck), inte skiftlägeskänsliga.</p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Attributvärdet; får inte innehålla <span class="codeph"> &lt;CR&gt; </span> eller <span class="codeph"> &lt;LF&gt; </span> tecken, såvida det inte föregås av ett omvänt snedstreck precis före radmatningstecknet. </p> </td> 
 </tr> 
</table>

* Tomt utrymme mellan variabler är valfritt.
* [!DNL Platform Server] ignorerar poster med okända attributnamn.
* Attributnamn kan bestå av en valfri kombination av ASCII-bokstäver, siffror och `-`, `_` och `.` tecken.
* Om samma attributnamn förekommer mer än en gång i samma attributfil gäller det senast påträffade attributnamnet.
* Använd `#` som första tecken för att markera en post som en kommentar som tolkaren ignorerar.
