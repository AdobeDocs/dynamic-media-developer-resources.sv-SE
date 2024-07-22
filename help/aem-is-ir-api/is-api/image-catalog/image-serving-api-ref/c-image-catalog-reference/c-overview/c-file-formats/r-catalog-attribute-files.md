---
description: Katalogattributfiler kan ha vilket namn som helst, men måste ha ett .ini-filsuffix. De kan enkelt underhållas med valfri textredigerare.
solution: Experience Manager
title: Katalogattributfiler
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# Katalogattributfiler{#catalog-attribute-files}

Katalogattributfiler kan ha vilket namn som helst, men måste ha ett .ini-filsuffix. De kan enkelt underhållas med valfri textredigerare.

Katalogattributfiler består av en uppsättning textposter, avgränsade med en `<CR>` (ASCII-kod `0xD`), en `<LF>` (ASCII-kod `0xA`) eller ett `<CR><LF>`-par. Varje post består av ett attributnamn och ett eller flera kommaavgränsade attributvärden:

`*`name`*= *`values`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> värden </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> värden</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> namn</span> </p> </td> 
  <td class="stentry"> <p>Attributnamn. Kan bestå av en eller flera bokstäver, siffror, - och _. Inte skiftlägeskänslig. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Attributvärde. Får inte innehålla <span class="codeph"> &lt;CR&gt;</span> eller <span class="codeph"> &lt;LF&gt;</span> tecken, såvida det inte föregås av ett omvänt snedstreck precis före radmatningstecknet. </p></td> 
 </tr> 
</table>

Tomt utrymme mellan variabler är valfritt.

Poster med okända attributnamn ignoreras av [!DNL Platform Server].

Attributnamn kan bestå av vilken kombination som helst av ASCII-bokstäver, siffror samt &quot;-&quot;, &quot;_&quot; och &quot;.&quot;.

Om samma attributnamn förekommer mer än en gång i samma attributfil gäller det senast påträffade attributnamnet.

Använd # som det första tecknet för att markera en post som en kommentar, som tolkas som en kommentar.
