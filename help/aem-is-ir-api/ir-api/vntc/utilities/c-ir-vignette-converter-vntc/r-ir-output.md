---
description: vntc genererar textdata som skickas till antingen stdern eller loggfilen.
seo-description: vntc genererar textdata som skickas till antingen stdern eller loggfilen.
seo-title: Utdata
solution: Experience Manager
title: Utdata
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f2041600-408f-481c-95fc-3c112def7b8a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---


# Utdata{#output}

vntc genererar textdata som skickas till antingen stdern eller loggfilen.

Data formateras som en `name=value`-egenskap per textpost. Strängvärden citeras inte. Varnings- och felmeddelanden skickas alltid till `stderr`, även om `-log` har angetts.

Vissa egenskaper kan förekomma flera gånger i samma utdata. Ett sekvensnummer, med början med 0, läggs till i namnet på dessa egenskaper, avgränsat med en punkt. Dessa egenskaper identifieras nedan med ett `. *`n`*`-suffix efter egenskapsnamnet.

Följande egenskaper genereras:

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>RGB-bakgrundsfärgen för kabinettformatet. Endast kabinettformat. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Standardversionen för utdatafilen. Även det högsta versionsnumret som den här versionen av <span class="filepath"> vntc</span> kan generera. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">fel.<span class="varname"> n</span>=<span class="varname"> sträng</span></span> </p></td> 
  <td class="stentry"> <p>Felmeddelande. Förekomsten av felmeddelanden brukar tyda på att inga utdatafiler har skapats eller att de inte är lämpliga för bildåtergivning. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-fil.<span class="varname"> n</span>=<span class="varname"> sträng</span></span> </p></td> 
  <td class="stentry"> <p>Den fullständiga sökvägen/namnet för alla utdatafiler, inklusive vinjetter, kabinettformatfiler, bilder med full upplösning och miniatyrbilder. Det finns ett filattribut för varje genererad fil (förutom loggfilen). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 1 </span> valideras om skåpet innehåller glasdörrar, annars 0. Endast kabinettformat. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Namnet på ICCProfile som är inbäddad i <span class="varname"> sourceFile</span>. </p> <p>Tom om <span class="varname"> sourceFile</span> inte är färghanterad. Endast vinjetter. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> sträng</span></span> </p></td> 
  <td class="stentry"> <p>Informationsmeddelande, t.ex. förloppsinformation. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 1 </span> valideras om  <span class="varname"> </span> sourceFile är en överordnad vinjettering, 0 om den har bearbetats tidigare med  <span class="filepath"> </span> vnUpdater eller  <span class="filepath"> vntc</span>. Endast vinjetter. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">överordnad=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 0 </span> valideras om  <span class="varname"> </span> sourceFile är ett kabinettformat som innehåller JPEG-bilddata (en varning genereras i det här fallet). Annars returneras 1. Skåp och fönster som endast omfattar formatfiler. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Den maximala minnesgräns som gäller för den pågående <span class="filepath"> vntc</span>-processen. <span class="varname"> </span> stringis either  <span class="varname"> ival</span>,  <span class="varname"> ivalK</span>,  <span class="varname"> ivalM</span>,  <span class="varname"> ivalG</span> eller  <span class="codeph">  </span> 0¥(disabled). Där <span class="varname"> K</span>, <span class="varname"> M</span> och <span class="varname"> G</span> refererar till kB (1024 byte), Megabyte (1048576 byte) och Gigabyte (107374182 4 byte). </p></td> 
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
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>För kabinettformat är objektupplösningen för källfilen<span class="varname"></span>. För vinjetter rekommenderas den här materialupplösningen för att ge bästa återgivningsresultat vid återgivning av utdatavjetter. Pixlar/tum (ppi). </p></td> 
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
  <td class="stentry"> <p>Den fullständiga sökvägen <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Filversionen av <span class="varname"> sourceFile</span>. </p></td> 
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
  <td class="stentry"> <p><span class="codeph"> Vntif </span> sourceFile är en  <span class="varname"> </span> vinjett,  <span class="codeph"> </span> vnCIF  <span class="varname"> </span> sourceFile är ett skåp eller  <span class="codeph"> </span> vnwif  <span class="varname"> </span> sourceFile är ett fönsteromfattande format. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Värdet som anges med <span class="codeph"> -version</span>, eller värdet på<span class="codeph"> defaultFileVersion</span> om<span class="codeph"> -version</span> inte angavs. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Kommaavgränsad lista över pixelstorlekarna för alla vyer i utdatavyjetten (den högupplösta vyn för pyramidvinjettering), för standardpanelbilden i en kabinettformatfil eller för den första opacitetsbilden i ett fönster som täcker formatfilen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 1 </span> valideras om kabinettformatet är texturerbart, annars 0. Finns inte för vinjetter och fönsteromslagsformatfiler. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">varning.<span class="varname"> n</span>=<span class="varname"> sträng</span></span> </p></td> 
  <td class="stentry"> <p>Varningsmeddelande (t.ex. när <span class="codeph"> -imagemap</span> har angetts, men inga mappningsdata hittas i vinjetteringen). </p></td> 
 </tr> 
</table>

