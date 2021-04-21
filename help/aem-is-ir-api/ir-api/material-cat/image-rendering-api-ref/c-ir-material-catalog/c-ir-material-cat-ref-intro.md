---
description: I det här dokumentet beskrivs materialkatalogen för Dynamic Media Image Rendering.
solution: Experience Manager
title: Introduktion
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---


# Introduktion{#introduction}

I det här dokumentet beskrivs materialkatalogen för Dynamic Media Image Rendering.

**Målgrupp**

Dokumentationen är avsedd för erfarna programmerare och webbplatsutvecklare som vill använda Dynamic Media Image Rendering för en webbplats eller ett anpassat program.

Det antas att läsaren känner till Dynamic Media Image Authoring and Image Rendering, allmänna HTTP-protokollstandarder och konventioner samt grundläggande bildterminologi.

**Dokumentkonventioner**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Literal </p> </td> 
  <td class="stentry"> <p>I syntaxavsnitt är icke-kursiv text literal. detta gäller inte för blanktecken och symbolerna [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>I beskrivande avsnitt är icke-kursiv text inom enkla citattecken literal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> parameter  </span> </p> </td> 
  <td class="stentry"> <p>Kursiv anger en variabel eller parameter som ska ersättas med ett faktiskt värde. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item  </span> </p> </td> 
  <td class="stentry"> <p>Ett namn med prefixet 'attribute::' refererar till ett bildkatalogsattribut. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> katalog::Item  </span> </td> 
  <td class="stentry"> <p>Ett namn med prefixet "katalog::" refererar till ett datakatalogfält. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p>Ett namn med prefixet 'icc:::' refererar till ett fält i ICC-färgprofilsmappningen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> makro::Item  </span> </p> </td> 
  <td class="stentry"> <p>Ett namn med "macro:::" som prefix refererar till ett fält i makrodefinitionstabellen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> linjaluppsättning::Item  </span> </p> </td> 
  <td class="stentry"> <p>Ett namn med prefixet 'ruleset::' refererar till ett element i en regeluppsättning för förbehandling av URL-adresser. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item  </span> </p> </td> 
  <td class="stentry"> <p>Ett namn med prefixet 'default:::' refererar till ett attribut i standardbildkatalogen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> vinjettering::Item  </span> </p> </td> 
  <td class="stentry"> <p>Ett namn med prefixet 'vignette::' refererar till ett fält i vinjetteringskartan. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> valfri </span> ] </p> </td> 
  <td class="stentry"> <p>Valfria syntaxelement omsluts av hakparenteser. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> valfri </span> ] </p> </td> 
  <td class="stentry"> <p>Det valfria syntaxelementet kan upprepas en eller flera gånger. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> objekt1  </span>|  <span class="varname"> objekt2  </span> </p> </td> 
  <td class="stentry"> <p>Ett lodrätt streck anger att syntaxobjektet till vänster eller objektet till höger kan användas. Exakt ett objekt måste markeras. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> group </span> } </p> </td> 
  <td class="stentry"> <p>Klammerparenteser används för att gruppera syntaxelement. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> group </span> } </p> </td> 
  <td class="stentry"> <p>Syntaxelementen i gruppen kan upprepas en eller flera gånger. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Tomt utrymme. </p> </td> 
  <td class="stentry"> <p>Tomt utrymme (blanksteg eller tabbar) tillåts inte i HTTP-begäranden. I det här dokumentet används ibland endast mellanrum mellan syntaktiska element för att skapa klarhet. </p> </td> 
 </tr> 
</table>

