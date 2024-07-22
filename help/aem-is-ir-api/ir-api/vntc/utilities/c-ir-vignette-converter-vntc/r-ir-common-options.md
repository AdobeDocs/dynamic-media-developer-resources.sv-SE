---
title: Vanliga alternativ
description: Följande alternativ kan användas oavsett typen av sourceFile.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Vanliga alternativ{#common-options}

Följande alternativ kan användas oavsett typen av sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> string </span> </span> </p> </td> 
  <td class="stentry"> <p>Mappen där utdatafilerna ska placeras (inklusive loggfilen, om <span class="codeph"> -log </span> har angetts). Det kan vara en absolut sökväg eller en relativ sökväg till aktuell arbetskatalog. Mapphierarkin skapas om den inte finns, men den gäller inte för filen som anges med <span class="codeph"> -log </span>. Om inget anges skrivs utdatafilerna till den mapp där <span class="varname"> sourceFile </span> finns. Om <span class="varname"> destFile </span> anges skrivs den alltid till den platsen och <span class="codeph"> -destpath </span> gäller bara för de sekundära utdatafilerna. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -image </span> </p> </td> 
  <td class="stentry"> <p>Om du anger det extraheras den (första) visningsbilden från vinjetteringen, en lämplig panelbild från ett skåpformat eller den första belysningsbilden för ett fönsteromslagsformat. Den extraherade bilden sparas som en TIFF-fil med full upplösning. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Förhindrar generering av målfiler. Det är praktiskt att snabbt extrahera attribut från en <span class="varname"> sourceFile </span>. Endast den valfria miniatyrbilden ( <span class="codeph"> -thumbwidth </span>), bilden ( <span class="codeph"> -image </span>) och loggfilerna ( <span class="codeph"> -log </span>) genereras. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Väljer förstörande JPEG-kodning för RGB och gråskalebilddata som är inbäddade i utdatafilen i stället för förlustfri PNG. Bilder med alfa (RGBA) sparas alltid med PNG-kodning. <span class="varname"> ival </span> anger JPEG-kvalitet (1...100); 85 eller högre rekommenderas. Standardvärdet är <span class="codeph"> -jpegquality 0 </span> som väljer PNG-kodning. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> path </span> </span> </p> </td> 
  <td class="stentry"> <p>Skapar en loggfil med den angivna sökvägen/namnet. De fullständiga sökvägarna för alla utdatafiler som skrivs till målmappen skrivs till loggfilen och ytterligare inställningar, till exempel versionsinformation och eventuella varningar eller fel som påträffas (mer information finns i <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Utdata </a> ). Ingen loggfil skapas om <span class="codeph"> -log </span> inte anges. I det här fallet skrivs all textutdata till <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Sänk prioriteten för <span class="filepath"> vntc </span> -processen. Den här processen kan användas så att <span class="filepath"> vntc </span> inte tar över en hel CPU när en vinjettering bearbetas. Det gör att operativsystemet kan ge mer tid till andra, viktigare, processer. <span class="varname"> ival </span> anger den lägre prioritetsprocenten (0..100). Standardvärdet är <span class="codeph"> -lowerpriority 0 </span>, vilket inte sänker prioriteten för <span class="filepath"> vntc </span> -processen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Ange den maximala mängd minne som <span class="filepath"> vntc </span> får använda i byte. När <span class="filepath"> vntc </span> når den maximala minnesgränsen avbryts bearbetningen och ett fel uppstår. <span class="varname">-värdet </span> anger den maximala minnesgränsen i byte (0..). 3 758 096 384 (3,5 GB). När <span class="varname">-värdet </span> är 0 inaktiveras den maximala minnesgränsen. Standardvärdet är <span class="codeph"> -maxmem 3221225472 </span> vilket innebär en maximal minnesgräns på 3 GB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator <span class="varname"> string </span> </span> </p> </td> 
  <td class="stentry"> <p>Anger avgränsaren mellan filnamnet och suffixet size/resolution för automatiskt genererade utdatafilnamn. Standardvärdet är - om inget anges. Ignoreras om <span class="varname"> destFile </span> eller <span class="codeph"> -info </span> har angetts. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -sharpen <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Möjliggör skärpa i bilder som samplas om (skalas) under bearbetningen. Gäller endast för miniatyrskärpa i kabinettfiler. </p> <p>Ange 0 om du vill inaktivera skärpa (standard), 1 om du vill aktivera normal skärpa, 2 om du vill aktivera oskarp maskering endast för intensitet eller 3 om du vill aktivera oskarp maskning för varje färgkomponent. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>Anger loggnivån. Standardvärdet är 1, vilket ger alla informations-, varnings- och felmeddelanden. Ange 0 om du vill inaktivera alla utom felmeddelanden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> amount </span> <span class="varname"> radius </span> <span class="varname"> threshold </span> </span> </p> </td> 
  <td class="stentry"> <p>Anger parametrar för oskarp maskning. Ignoreras om <span class="codeph"> -sharpen </span> är inställd på 0 eller 1. Krävs om <span class="codeph"> -sharpen </span> är inställd på 2 eller 3. <span class="varname"> amount </span> är ett reellt värde i intervallet 0.0...500.0, <span class="varname"> radius </span> är ett reellt värde i intervallet 0.0...10.0 och <span class="varname"> threshold </span> är ett heltal mellan 0 och 255. Mer information finns i beskrivningen av <span class="codeph"> op_usm= </span> i Image Serving Protocol Reference. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Verifiera att den angivna vinjetteringen är en riktig produktionsvolym. <span class="varname">-värdet </span> representerar den lägsta filversionen av vinjetteringen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Filversion för utdatafilen. Om den anges måste den vara 0 eller en giltig vinjettfilversion (inte större än standardfilversionen). Om värdet är 0 eller inte anges skapas utdatafilen med den senaste filversionen. Ignoreras om <span class="codeph"> -info </span> har angetts. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>Returnerar versionsinformation för det här verktyget. Ange utan filnamn och andra alternativ. </p> </td> 
 </tr> 
</table>
