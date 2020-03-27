---
description: Överför filer från angivna serverkataloger regelbundet.
seo-description: Överför filer från angivna serverkataloger regelbundet.
seo-title: UploadDirectoryJob
solution: Experience Manager
title: UploadDirectoryJob
topic: Scene7 Image Production System API
uuid: 6e6ae415-7c54-4bbb-aa98-ff9a77d956b0
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# UploadDirectoryJob{#uploaddirectoryjob}

Överför filer från angivna serverkataloger regelbundet.

Syntax

## Parametrar {#section-69c07f4e7b2e4a0fba143ffaa9f4d48f}

<table id="table_6E40A78846F444BDB8E437413B90CFCE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Namn </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AutoColorOptions</span> </td> 
   <td colname="col3"> <p>Alternativ för automatisk bildbeskärning (baserat på färg). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>En matris med skript för automatisk set-generering som ska användas för överförda filer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>Tar bort tomt utrymme från bildkanterna baserat på genomskinlighet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>Alternativ som du kan ange under en överföring. Uppsättningen påverkar hur färgen hanteras för överföringen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> <p>Om en mask ska skapas när den överförs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> <p>IPS-mapp för filerna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> <p>Val av e-postinställningar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:IllustratorOptions</span> </td> 
   <td colname="col3"> <p>Alternativ för överföring av Illustrator-filer till bildservern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> <p>Om undermappar ska inkluderas vid överföring. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:InDesignOptions</span> </td> 
   <td colname="col3"> <p>Alternativ för överföring av InDesign-filer till servern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>Maskera bakgrunden för markerade bilder. På så sätt kan du täcka över dem i andra lager med en genomskinlighet utanför objektbilden. </p> <p>Valfritt. </p> <p>Se <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>Manuella bildbeskärningsalternativ. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:MediaOptions</span> </td> 
   <td colname="col3"> <p>Alternativ som gör att du kan ange en miniatyrbild från videon. </p> <p>Se <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> Mediealternativ</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> skriv över</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> <p>Alternativ för filöverföring, överskrivning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:PDFOptions</span> </td> 
   <td colname="col3"> <p>Alternativ för överföring av PDF-filer till bildservern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>Alternativ för att överföra Photoshop-filer till bildservern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> <p>URL:en för filöverföringsmålet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublish</span> </span>Job </td> 
   <td colname="col2"> <span class="codeph"> typer:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> <p>Information om ett publiceringsjobb för bildåtergivning som körs när överföringen är klar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ImageServingPublishJob</span> </td> 
   <td colname="col3"> <p>Information om en bild som visar ett publiceringsjobb som körs när överföringen är klar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> <p>Om bara filer ska överföras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>Alternativ för överföring av PostScript-filer till bildservern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:VideoPublishJob</span> </td> 
   <td colname="col3"> <p>Information om ett videopubliceringsjobb som körs när överföringen är klar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> <p>Kontrollerar bevarande av befintliga beskärningsdefinitioner. Standardvärdet är true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> <p>Styr om publiceringstillståndet för en befintlig resurs bevaras när den skrivs över. Om den inte anges används företagets standardinställning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> processMetadataFiles</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> <p>Om separata XML-metadatafiler ska bearbetas för det här jobbet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:HandleArray</span> </td> 
   <td colname="col3"> <p>Array med projektreferenser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> <p>Avgör om filer är markerade som klara för publicering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDir</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> <p>Källkatalog för överföring. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:UnCompressOptions</span> </td> 
   <td colname="col3"> <p>Extrahera och bearbeta innehållet i överförda TAR/ZIP-filer med dessa valfria inställningar. </p> <p>Se <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> AvkomprimeraAlternativ</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>Alternativ som gör att du kan styra inställningarna för oskarp mask när du skapar en optimerad TIF-pyramidfil. Använd de här inställningarna för att förbättra bildens skärpa. </p> <p>Se <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_unsharp_mask_options.html"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> xmpKeywords</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:sträng</span> </p> </td> 
   <td colname="col3"> <p>Ytterligare metadataalternativ för allt i överföringsjobbet </p> </td> 
  </tr> 
 </tbody> 
</table>

## Anteckningar {#section-637405ff7e0b4a71b83fd359b92fa0c2}

Du kan t. `CropOptions`ex. bara välja något av följande:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Du kan t. `PublishJob`ex. bara välja något av följande:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`

