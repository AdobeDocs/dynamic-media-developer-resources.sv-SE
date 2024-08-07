---
description: vntc genererar textdata som skickas till antingen stdern eller loggfilen.
solution: Experience Manager
title: Utdata
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Utdata{#output}

vntc genererar textdata som skickas till antingen stdern eller loggfilen.

Data är formaterade som en `name=value`-egenskap per textpost. Strängvärden citeras inte. Varnings- och felmeddelanden skickas alltid till `stderr`, även om `-log` har angetts.

Vissa egenskaper kan förekomma flera gånger i samma utdata. Ett sekvensnummer, med början med 0, läggs till i namnet på dessa egenskaper, avgränsat med en punkt. Sådana egenskaper identifieras nedan med suffixet `. *`n`*` efter egenskapsnamnet.

Följande egenskaper genereras:

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>RGB bakgrundsfärg för kabinettformatet. Endast kabinettformat. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Standardversionen för utdatafilen. Även det högsta filversionsnumret som den här versionen av <span class="filepath"> vntc</span> kan generera. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">fel.<span class="varname"> n</span>=<span class="varname"> sträng </span></span> </p></td> 
  <td class="stentry"> <p>Felmeddelande. Förekomsten av felmeddelanden brukar tyda på att inga utdatafiler har skapats eller att de inte är lämpliga för bildåtergivning. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">fil.<span class="varname"> n</span>=<span class="varname"> sträng </span></span> </p></td> 
  <td class="stentry"> <p>Den fullständiga sökvägen/namnet för alla utdatafiler, inklusive vinjetter, kabinettformatfiler, bilder med full upplösning och miniatyrbilder. Det finns ett filattribut för varje genererad fil (förutom loggfilen). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> är 1 om skåpet innehåller glasdörrar, annars 0. Endast kabinettformat. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Namnet på ICCProfile som är inbäddad i <span class="varname"> sourceFile </span>. </p> <p>Tom om <span class="varname"> sourceFile </span> inte är färghanterad. Endast vinjetter. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> sträng </span></span> </p></td> 
  <td class="stentry"> <p>Informationsmeddelande, till exempel förloppsinformation. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname">-värdet </span> är 1 om <span class="varname"> sourceFile </span> är en huvudvinjettering, 0 om den tidigare har bearbetats med <span class="filepath"> vnUpdate </span> eller <span class="filepath"> vntc</span>. Endast vinjetter. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> är 0 om <span class="varname"> sourceFile </span> är ett kabinettformat som innehåller JPEG-bilddata (en varning skickas också i det här fallet), annars 1. Skåp och fönster som endast omfattar formatfiler. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Den maximala minnesgränsen som gäller för den pågående <span class="filepath"> vntc</span>-processen. <span class="varname"> sträng </span> är antingen <span class="varname"> ival</span>, <span class="varname"> ivalK</span>, <span class="varname"> ivalM</span>, <span class="varname"> ivalG</span> eller <span class="codeph"> 0</span> (inaktiverad). Där <span class="varname"> K</span>, <span class="varname"> M</span> och <span class="varname"> G</span> refererar till kB (1024 byte), Megabyte (1048576 byte) och Gigabyte (1073741824 byte). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Skalan för pyramidnivån med den lägsta upplösningen i utdatavinjetten. Finns endast om <span class="codeph"> -pyramid</span> har angetts. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Antalet material som har sparats i <span class="varname"> sourceFile</span>. Endast vinjetter. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Antalet panelbilder i den här kabinettformatfilen. Endast kabinettformat. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Antalet pyramidnivåer i utdatavvignetten. Finns endast om -pyramid anges. Endast vinjetter. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">pyramid=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>0 om käll- eller målvinjetteringen har pyramidstruktur. Endast vinjetter. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">upplösning=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>För kabinettformat är objektupplösningen för <span class="varname"> sourceFile</span>. För vinjetter rekommenderas den här materialupplösningen för att ge bästa återgivningsresultat vid återgivning av utdatavjetter. Pixlar/tum (ppi). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Den minsta objektupplösningen i utdatavvignetten. Endast vinjetter. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Den genomsnittliga objektupplösningen i utdatavvignetten. Endast vinjetter. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Den fullständigt kvalificerade sökvägen <span class="varname"> sourceFile </span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Filversionen för <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Pixelstorleken för indatavvinjetteringen, standardpanelbilden i en kabinettformatfil eller den första opacitetsbilden i ett fönster som täcker formatfilen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Typ av fönsterhölje (endast fönsterformat): </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=vågrät skugga eller persienner </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=vertikala blinkningar </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=korta draperier med full bredd </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=kort vänster/höger radband </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=helbreda draperier </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=vänster/höger fullängdsband </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=cafédram </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=värde </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> sträng</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> vnt</span> om <span class="varname"> sourceFile </span> är en vinjett, <span class="codeph"> vnc </span> om <span class="varname"> sourceFile </span> är ett kabinettformat, eller <span class="codeph"> vnw</span> om <span class="varname"> sourceFile </span> är ett fönsteromfattande format. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Värdet som angavs med <span class="codeph"> -version </span> eller värdet <span class="codeph"> defaultFileVersion </span> om <span class="codeph"> -version </span> inte angavs. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Kommaavgränsad lista över pixelstorlekarna för alla vyer i utdatavyjetten (den högupplösta vyn för pyramidvinjettering), för standardpanelbilden i en kabinettformatfil eller för den första opacitetsbilden i ett fönster som täcker formatfilen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname">-värdet </span> är 1 om kabinettformatet är texturerbart, annars 0. Finns inte för vinjetter och fönsteromslag. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">varning.<span class="varname"> n</span>=<span class="varname"> sträng </span></span> </p></td> 
  <td class="stentry"> <p>Varningsmeddelande (t.ex. när <span class="codeph"> -imagemap</span> har angetts, men inga mappningsdata hittas i vinjetteringen). </p></td> 
 </tr> 
</table>
