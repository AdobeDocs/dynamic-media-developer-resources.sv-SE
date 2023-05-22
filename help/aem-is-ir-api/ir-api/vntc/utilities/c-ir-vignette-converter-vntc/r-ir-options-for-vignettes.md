---
description: Följande alternativ styr bearbetningen av vinjettfiler. De ignoreras om sourceFile inte är en vinjett.
solution: Experience Manager
title: Alternativ för vinjetter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Alternativ för vinjetter{#options-for-vignettes}

Följande alternativ styr bearbetningen av vinjettfiler. De ignoreras om sourceFile inte är en vinjett.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -contents</span> </p></td> 
  <td class="stentry"> <p>Skapar en XML-fil som representerar objekthierarkin och inkluderar valda objektattribut. Innehållet i filen är detsamma som det returneras av <span class="codeph"> req=contents</span> -kommando. Filen har samma namn som källfilen, men med en <span class="filepath"> .xml</span> suffix. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>Beskär vinjetteringen före skalning. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> är beskärningsrektangelns övre vänstra hörn, och <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> hei</span></span> är beskärningsrektangelns storlek. Värden är pixelkoordinater i förhållande till den högupplösta vybilden för källvinjetteringen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> widn</span><span class="varname"> hein</span></span> </p> </td> 
  <td class="stentry"> <p>Beskär vinjetteringen före skalning. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> är beskärningsrektangelns övre vänstra hörn, och <span class="codeph"><span class="varname"> widn</span>,<span class="varname"> hein</span></span> är beskärningsrektangelns storlek. Värdena normaliseras i förhållande till källvinjetteringens visningsbild och måste vara mellan 0.0...1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> widn</span></span> och <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> hein</span></span> får inte vara större än 1,0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -embedmaterials</span> </p></td> 
  <td class="stentry"> <p>Behåll inbäddat material i utdatavärjningen. Som standard tas material bort från utdatavärjningen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>En eller flera höjder för utdatavinjettering i pixlar. Ignoreras om -info anges. <span class="varname"> ival</span> kan vara 0, vilket anger bredden på indatavvinjetteringen. Se <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vinjettskalförändring</a> för detaljerad information. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Aktivera extrahering av bildschemafilen från vinjetteringen. Kartdata skrivs till en HTML-fil som bara innehåller en <span class="codeph"> &lt;map&gt;</span> -element. Utdatafilen får samma namn som utdatabildfilen, men med en <span class="filepath"> .htm</span> suffix. Ett varningsmeddelande genereras och ingen fil skapas om kommandot har angetts, men det inte finns några mappningsdata i vinjetteringen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profile</span> </p></td> 
  <td class="stentry"> <p>Sparar en kopia av ICC-profilen som är inbäddad i vinjetteringen till en fil. Ett varningsmeddelande genereras och ingen ICC-profilfil skapas om kommandot har angetts, men det inte finns någon ICC-profil i vinjetteringen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -pyramid</span> </p></td> 
  <td class="stentry"> <p>Skapar en pyramidvinjettering. Krävs när återgivna bilder ska visas med Dynamic Media zoomningsvisningsprogram. Se <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vinjettskalförändring</a> för ytterligare information. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Pixelns bredd- och höjdbegränsning för miniatyrbilden. Om den anges, en JPEG-bild som inte är bredare och inte längre än <span class="varname"> ival</span> genereras från vinjettvybilden, en panelbild av kabinettformatfilen eller belysningskartan för det första formatet i fönsteromslagsformatfilen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>En eller flera utdatavärdesbredder i pixlar. Ignoreras om <span class="codeph"> -info</span> har angetts. <span class="varname"> ival</span> kan vara 0, vilket anger höjden på indatavvinjetteringen. Se <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vinjettskalförändring</a> för detaljerad information. </p></td> 
 </tr> 
</table>
