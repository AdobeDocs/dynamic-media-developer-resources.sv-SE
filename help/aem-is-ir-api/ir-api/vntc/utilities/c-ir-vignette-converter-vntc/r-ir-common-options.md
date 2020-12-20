---
description: Följande alternativ kan användas oavsett typen av sourceFile.
seo-description: Följande alternativ kan användas oavsett typen av sourceFile.
seo-title: Vanliga alternativ
solution: Experience Manager
title: Vanliga alternativ
topic: Scene7 Image Serving - Image Rendering API
uuid: fdf09873-4102-4ed6-a315-a87cba5c44c7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 0%

---


# Vanliga alternativ{#common-options}

Följande alternativ kan användas oavsett typen av sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath- <span class="varname"> sträng  </span> </span> </p> </td> 
  <td class="stentry"> <p>Mappen som utdatafilerna ska placeras i (inklusive loggfilen om <span class="codeph"> -log </span> har angetts). Kan vara en absolut sökväg eller relativ till den aktuella arbetskatalogen. Mapphierarkin skapas om den inte finns. Gäller inte för filen som anges med <span class="codeph"> -log </span>. Om inget anges skrivs utdatafilerna till den mapp där <span class="varname"> sourceFile </span> finns. Om <span class="varname"> destFile </span> anges skrivs den alltid till den platsen och <span class="codeph"> -destpath </span> gäller bara för de sekundära utdatafilerna. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -image  </span> </p> </td> 
  <td class="stentry"> <p>Om du anger det extraheras den (första) visningsbilden från vinjetteringen, en lämplig panelbild från ett skåpformat eller den första belysningsbilden för ett fönsteromslagsformat. Den extraherade bilden sparas som en TIFF-fil med full upplösning. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info  </span> </p> </td> 
  <td class="stentry"> <p>Förhindrar generering av målfiler. Det är praktiskt att snabbt extrahera attribut från <span class="varname"> sourceFile </span>. Endast den valfria miniatyrbilden ( <span class="codeph"> -thumbwidth </span>), bilden ( <span class="codeph"> -image </span>) och loggfilerna ( <span class="codeph"> -log </span>) genereras. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Väljer JPEG-kodning med dataförlust för RGB och gråskalebilddata som är inbäddade i utdatafilen i stället för förlustfri PNG. Bilder med alfa (RGBA) sparas alltid med PNG-kodning. <span class="varname"> ival  </span> anger JPEG-kvaliteten (1...100), 85 eller högre rekommenderas. Standardvärdet är <span class="codeph"> -jpegquality 0 </span>, som väljer PNG-kodning. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log  <span class="varname"> path  </span> </span> </p> </td> 
  <td class="stentry"> <p>Skapar en loggfil med den angivna sökvägen/namnet De fullständiga sökvägarna för alla utdatafiler som skrivs till målmappen skrivs till loggfilen, samt ytterligare inställningar, till exempel versionsinformation och eventuella varningar eller fel som påträffas (mer information finns i <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Utdata </a>). Ingen loggfil skapas om <span class="codeph"> -log </span> inte har angetts; I det här fallet skrivs all text till <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowPriority  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Sänk prioriteten för <span class="filepath"> vntc </span>-processen. Detta kan användas så att <span class="filepath"> vntc </span> inte tar över en hel processor när en vinjettering bearbetas. Det gör att operativsystemet kan ge mer tid till andra, viktigare, processer. <span class="varname"> ival  </span> anger den lägre prioriteten i procent (0..100). Standardvärdet är <span class="codeph"> -lowerpriority 0 </span>, vilket inte sänker prioriteten för <span class="filepath"> vntc </span>-processen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Ange den maximala mängd minne som <span class="filepath"> vntc </span> får använda i byte. När <span class="filepath"> vntc </span> når den maximala minnesgränsen avbryts bearbetningen och ett fel uppstår. <span class="varname"> ival  </span> anger den maximala minnesgränsen i byte (0.. 3 758 096 384 (3,5 GB). När <span class="varname">-värdet </span> är 0 inaktiveras den maximala minnesgränsen. Standardvärdet är <span class="codeph"> -maxmem 3221225472 </span>, vilket innebär en maximal minnesgräns på 3 GB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator "  <span class="varname"> string  </span>"  </span> </p> </td> 
  <td class="stentry"> <p>Anger avgränsaren mellan filnamnet och suffixet size/resolution för automatiskt genererade utdatafilnamn. Standardvärdet är - om inget anges. Ignoreras om <span class="varname"> destFile </span> eller <span class="codeph"> -info </span> har angetts. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -sharpen  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Möjliggör skärpa i bilder som samplas om (skalas) under bearbetningen. Gäller endast för miniatyrskärpa när det gäller kabinettformatfiler. </p> <p>Ange 0 om du vill inaktivera skärpa (standard), 1 om du vill aktivera normal skärpa, 2 om du vill aktivera oskarp maskering endast för intensitet eller 3 om du vill aktivera oskarp maskning för varje färgkomponent. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel  </span> </p> </td> 
  <td class="stentry"> <p>Anger loggnivån. Standardvärdet är 1, vilket ger alla informations-, varnings- och felmeddelanden. Ange 0 om du vill inaktivera alla utom felmeddelanden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm  <span class="varname"> beloppets  </span> <span class="varname"> radie- </span> <span class="varname"> tröskelvärde  </span> </span> </p> </td> 
  <td class="stentry"> <p>Anger parametrar för oskarp maskning. Ignoreras om <span class="codeph"> -sharpen </span> är inställd på 0 eller 1; krävs om <span class="codeph"> -sharpen </span> är inställd på 2 eller 3. <span class="varname"> mängd  </span> är ett reellt värde i intervallet 0.0...500.0,  <span class="varname"> radius  </span> är ett reellt värde i intervallet 0.0...10.0 och  <span class="varname"> tröskelvärdet  </span> är ett heltal mellan 0 och 255. Mer information finns i beskrivningen av <span class="codeph"> op_usm= </span> i Image Serving Protocol Reference. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Verifiera att den angivna vinjetteringen är en riktig produktionsvolym. <span class="varname"> ival  </span> representerar den lägsta filversionen av vinjetteringen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Filversion för utdatafilen. Om det anges måste det vara 0 eller en giltig vinjettfilversion (inte större än standardfilversionen). Om värdet är 0 eller inte anges skapas utdatafilen med den senaste filversionen. Ignoreras om <span class="codeph"> -info </span> har angetts. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo  </span> </p> </td> 
  <td class="stentry"> <p>Returnerar versionsinformation för det här verktyget. Ange utan filnamn och andra alternativ. </p> </td> 
 </tr> 
</table>

