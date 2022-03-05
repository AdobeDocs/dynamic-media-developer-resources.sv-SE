---
description: Följande alternativ kan användas oavsett typen av sourceFile.
solution: Experience Manager
title: Vanliga alternativ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# Vanliga alternativ{#common-options}

Följande alternativ kan användas oavsett typen av sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> string </span> </span> </p> </td> 
  <td class="stentry"> <p>Mappen där utdatafilerna ska placeras (inklusive loggfilen, om <span class="codeph"> -log </span> anges). Kan vara en absolut sökväg eller relativ till den aktuella arbetskatalogen. Mapphierarkin skapas om den inte finns. Gäller inte för filen som anges med <span class="codeph"> -log </span>. Om inget anges skrivs utdatafilerna till den mapp där <span class="varname"> sourceFile </span> finns. If <span class="varname"> destFile </span> anges skrivs den alltid till den platsen, och <span class="codeph"> -destpath </span> gäller endast för de sekundära utdatafilerna. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -image </span> </p> </td> 
  <td class="stentry"> <p>Om du anger det extraheras den (första) visningsbilden från vinjetteringen, en lämplig panelbild från ett skåpformat eller den första belysningsbilden för ett fönsteromslagsformat. Den extraherade bilden sparas som en TIFF-fil med full upplösning. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Förhindrar generering av målfiler. Använd för att snabbt extrahera attribut från <span class="varname"> sourceFile </span>. Endast den valfria miniatyrbilden ( <span class="codeph"> -thumbwidth </span>), bild ( <span class="codeph"> -image </span>) och loggfiler ( <span class="codeph"> -log </span>) genereras. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Väljer förstörande JPEG-kodning för RGB och gråskalebilddata som är inbäddade i utdatafilen i stället för förlustfri PNG. Bilder med alfa (RGBA) sparas alltid med PNG-kodning. <span class="varname"> ival </span> JPEG (1...100). 85 eller högre rekommenderas. Standard är <span class="codeph"> -jpegquality 0 </span>, som väljer PNG-kodning. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> bana </span> </span> </p> </td> 
  <td class="stentry"> <p>Skapar en loggfil med den angivna sökvägen/namnet De fullständiga sökvägarna för alla utdatafiler som skrivs till målmappen skrivs till loggfilen, samt ytterligare inställningar, som versionsinformation och eventuella varningar eller fel som påträffas (se <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Utdata </a> för mer information). Ingen loggfil skapas om <span class="codeph"> -log </span> inte har angetts, i det här fallet skrivs all text till <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Minska prioriteten för <span class="filepath"> vntc </span> -processen. Detta kan användas så att <span class="filepath"> vntc </span> tar inte över en hel processor när en vinjett bearbetas. Det gör att operativsystemet kan ge mer tid till andra, viktigare, processer. <span class="varname"> ival </span> anger den lägre prioriteten i procent (0..100). Standard är <span class="codeph"> -lowerpriority 0 </span>som inte sänker prioriteten för <span class="filepath"> vntc </span> -processen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Ange den maximala mängden minne som <span class="filepath"> vntc </span> får användas i byte. När <span class="filepath"> vntc </span> når maximal minnesgräns, avbryter bearbetningen och skapar ett fel. <span class="varname"> ival </span> anger den maximala minnesgränsen i byte (0.. 3 758 096 384 (3,5 GB). När <span class="varname"> ival </span> är 0, maximal minnesgräns är inaktiverad. Standard är <span class="codeph"> -maxmem 3221225472 </span>, vilket innebär en maximal minnesgräns på 3 GB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator " <span class="varname"> string </span>" </span> </p> </td> 
  <td class="stentry"> <p>Anger avgränsaren mellan filnamnet och suffixet size/resolution för automatiskt genererade utdatafilnamn. Standardvärdet är - om inget anges. Ignoreras om <span class="varname"> destFile </span> eller <span class="codeph"> -info </span> har angetts. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -sharpen <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Möjliggör skärpa i bilder som samplas om (skalas) under bearbetningen. Gäller endast för miniatyrskärpa när det gäller kabinettformatfiler. </p> <p>Ange 0 om du vill inaktivera skärpa (standard), 1 om du vill aktivera normal skärpa, 2 om du vill aktivera oskarp maskering endast för intensitet eller 3 om du vill aktivera oskarp maskning för varje färgkomponent. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>Anger loggnivån. Standardvärdet är 1, vilket ger alla informations-, varnings- och felmeddelanden. Ange 0 om du vill inaktivera alla utom felmeddelanden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> belopp </span> <span class="varname"> radie </span> <span class="varname"> tröskelvärde </span> </span> </p> </td> 
  <td class="stentry"> <p>Anger parametrar för oskarp maskning. Ignoreras om <span class="codeph"> -sharpen </span> är inställt på 0 eller 1, krävs om <span class="codeph"> -sharpen </span> är inställd på 2 eller 3. <span class="varname"> belopp </span> är ett reellt värde i intervallet 0,0 till 500,0, <span class="varname"> radie </span> är ett reellt värde i intervallet 0,0...10,0 och <span class="varname"> tröskelvärde </span> är ett heltal mellan 0 och 255. Se beskrivningen av <span class="codeph"> op_usm= </span> i Image Serving Protocol Reference för ytterligare information. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Verifiera att den angivna vinjetteringen är en riktig produktionsvolym. <span class="varname"> ival </span> representerar den lägsta filversionen av vinjetteringen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Filversion för utdatafilen. Om det anges måste det vara 0 eller en giltig vinjettfilversion (inte större än standardfilversionen). Om värdet är 0 eller inte anges skapas utdatafilen med den senaste filversionen. Ignoreras om <span class="codeph"> -info </span> har angetts. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>Returnerar versionsinformation för det här verktyget. Ange utan filnamn och andra alternativ. </p> </td> 
 </tr> 
</table>
