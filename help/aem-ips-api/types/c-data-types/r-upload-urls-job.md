---
description: Överför URL:er från den plats där du vill hämta filer.
seo-description: Överför URL:er från den plats där du vill hämta filer.
seo-title: UploadUrlsJob
solution: Experience Manager
title: UploadUrlsJob
topic: Dynamic Media Image Production System API
uuid: 6140e969-bf61-4b62-9a60-29609626b0b4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---


# UploadUrlsJob{#uploadurlsjob}

Överför URL:er från den plats där du vill hämta filer.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AutoColorCropOptions</span> </td> 
   <td colname="col3"> Alternativ för automatisk beskärning av bilder baserat på färg. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AutoSetCreationOptions</span> </td> 
   <td colname="col3"> En matris med skript för automatisk set-generering som ska användas för överförda filer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> Tar bort tomt utrymme från bildkanterna baserat på genomskinlighet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Om en mask ska skapas. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ColorManagementOptions</span> </td> 
   <td colname="col3"> Alternativ som du kan ange under en överföring. Uppsättningen påverkar hur färgen hanteras för överföringen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Val av e-postinställningar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:IllustratorOptions</span> </td> 
   <td colname="col3"> Alternativ för överföring av Illustrator-filer till Image Server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:InDesignOptions</span> </td> 
   <td colname="col3"> Alternativ för överföring av InDesign-filer till servern. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3">Maskera bakgrunden för markerade bilder. På så sätt kan du täcka över dem i andra lager med en genomskinlighet utanför objektbilden. Valfritt. Se<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ManualCropOptions</span> </td> 
   <td colname="col3"> Alternativ för manuell beskärning av bilder. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:MediaOptions</span> </td> 
   <td colname="col3">Alternativ som gör att du kan ange en miniatyrbild från videon. Se <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numUrls</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3">Returnerar antalet URL-adresser som har skickats i ett jobb. Används av <a href="../../operations/c-operations-intro/c-methods/r-get-active-jobs.md#reference-67483cbd71d04042b48434d886e8a7a0" format="dita" scope="local"> getActiveJobs</a> och <a href="../../operations/c-operations-intro/c-methods/r-get-scheduled-jobs.md#reference-2bab1861325f4bff84c879d1efa9146e" format="dita" scope="local"> getScheduledJobs</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> skriv över</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Om filer ska skrivas över vid överföring. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:PDFOptions</span> </td> 
   <td colname="col3"> Alternativ för överföring av PDF-filer till bildservern. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:PhotoshopOptions</span> </td> 
   <td colname="col3"> Alternativ för överföring av Photoshop-filer till Image Server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Den URL som filerna överförs till. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> Information om ett publiceringsjobb för bildåtergivning som körs när överföringen är klar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Alla mediealternativ. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:PostScriptOptions</span> </td> 
   <td colname="col3"> Alternativ för överföring av PostScript-filer till Image Server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:VideoPublishJob</span> </td> 
   <td colname="col3"> Information om ett videopubliceringsjobb som körs när överföringen är klar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Kontrollerar bevarande av befintliga beskärningsdefinitioner. Standardvärdet är true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Styr om publiceringstillståndet för en befintlig resurs bevaras när den skrivs över. Om den inte anges används företagets standardinställning. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:HandleArray</span> </td> 
   <td colname="col3"> Array med projektreferenser. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Anger om filerna är markerade som klara för publicering. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:UnCompressOptions</span> </td> 
   <td colname="col3">Extrahera och bearbeta innehållet i överförda TAR/ZIP-filer med dessa valfria inställningar. Se <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:UnsharpMaskOptions</span> </td> 
   <td colname="col3">Alternativ som gör att du kan styra inställningarna för oskarp mask när du skapar en optimerad TIF-pyramidfil. Använd de här inställningarna för att förbättra bildens skärpa. Se <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> urlArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:UrlArray</span> </td> 
   <td colname="col3"> En array med URL:er som du vill överföra. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> <p>Ytterligare ett metadataalternativ för allt i överföringsjobbet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Anteckningar {#section-637405ff7e0b4a71b83fd359b92fa0c2}

För `CropOptions` kan du bara välja något av följande:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

För `PublishJob` kan du bara välja något av följande:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`

