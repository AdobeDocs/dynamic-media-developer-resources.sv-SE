---
title: Katalogattributfiler
description: Katalogattributfiler kan ha vilket namn som helst, men måste ha ett .ini-filsuffix. De kan enkelt underhållas med valfri textredigerare.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Katalogattributfiler{#catalog-attribute-files}

Katalogattributfiler kan ha vilket namn som helst, men måste ha ett `.ini` filsuffix. De kan enkelt underhållas med valfri textredigerare.

Katalogattributfiler består av en uppsättning textposter, avgränsade med en enda `<CR>` (ASCII-kod 0xD), en `<LF>` (ASCII-kod 0xA), eller `<CR><LF>` par. Varje post består av ett attributnamn och ett eller flera kommaavgränsade attributvärden:

`*`name`*= *`value`*&#42;[, *`value`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Attributnamn; kan bestå av en eller flera bokstäver, siffror, '-' och '_', inte skiftlägeskänsliga. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Attributvärde; får inte innehålla <span class="codeph"> &lt;cr&gt; </span>, eller <span class="codeph"> &lt;lf&gt; </span> om det inte föregås av ett omvänt snedstreck precis före radmatningstecknet. </p> </td> 
 </tr> 
</table>

* Tomt utrymme mellan variabler är valfritt.
* Poster med okända attributnamn ignoreras av [!DNL Platform Server].
* Attributnamn kan bestå av vilken kombination som helst av ASCII-bokstäver, siffror och&quot;-&quot;,&quot;_&quot; och&quot;.&quot;
* Om samma attributnamn förekommer mer än en gång i samma attributfil gäller det senast påträffade attributnamnet.
* Använd &#39;#&#39; som första tecken för att markera en post som en kommentar som tolkaren ignorerar.
