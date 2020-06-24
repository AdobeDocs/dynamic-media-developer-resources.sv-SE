---
description: Jobbtyp som tillåter ombearbetning av tidigare överförda primära filer, inklusive återgivning av PDF-filer och omoptimering av bilder.
seo-description: Jobbtyp som tillåter ombearbetning av tidigare överförda primära filer, inklusive återgivning av PDF-filer och omoptimering av bilder.
seo-title: ÅterbearbetaResurserJobb
solution: Experience Manager
title: ÅterbearbetaResurserJobb
topic: Scene7 Image Production System API
uuid: 5b4aa838-0fb4-4ae8-be5a-8ce1e1487127
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---


# ÅterbearbetaResurserJobb{#reprocessassetsjob}

Jobbtyp som tillåter ombearbetning av tidigare överförda primära filer, inklusive återgivning av PDF-filer och omoptimering av bilder.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Namn </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Resurshandtag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolesk</span> </p> </td> 
   <td colname="col3"> <p>Anger om filerna är markerade som klara för publicering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolesk</span> </p> </td> 
   <td colname="col3"> <p>Styr om publiceringstillståndet för en befintlig resurs bevaras när den skrivs över. Om den inte anges används företagets standardinställning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolesk</span> </p> </td> 
   <td colname="col3"> <p>Om en mask ska skapas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolesk</span> </p> </td> 
   <td colname="col3">Kontrollerar bevarande av befintliga beskärningsdefinitioner. Standardvärdet är <span class="codeph"> true</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Manuella beskärningsalternativ. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ för automatisk beskärning av bilder baserat på färg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Tar bort tomt utrymme från bildkanterna baserat på genomskinlighet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ för att överföra Photoshop-filer till bildservern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ för överföring av PostScript-filer till bildservern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ för överföring av PDF-filer till bildservern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ för A/V-mediefiler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ för överföring av Illustrator-filer till Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ som du kan ange under en överföring. Uppsättningen påverkar hur färgen hanteras för överföringen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>En matris med skript för automatisk set-generering som ska användas för överförda filer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>En array med projektreferenser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:sträng</span> </p> </td> 
   <td colname="col3"> <p>Alternativ för e-postinställningar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolesk</span> </p> </td> 
   <td colname="col3"> <p>Om bara filer ska överföras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:sträng</span> </p> </td> 
   <td colname="col3"> <p>URL till filöverföringsplats. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Jobbinformation för en bild som visar ett publiceringsjobb som ska köras när överföringen är slutförd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Jobbinformation för ett publiceringsjobb för bildåtergivning som ska köras när överföringen är slutförd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Jobbinformation för ett videopubliceringsjobb som ska köras när överföringen är slutförd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ för överföring av InDesign-filer till bildservern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Maskera bakgrunden för markerade bilder. På så sätt kan du täcka över dem i andra lager med en genomskinlighet utanför objektbilden. </p> <p>Valfritt. </p> <p>Se<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> BlockeraBakgrundAlternativ</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:UnsharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ som gör att du kan styra inställningarna för oskarp mask när du skapar en optimerad TIF-pyramidfil. Använd de här inställningarna för att förbättra bildens skärpa. </p> <p>Se <a href="https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Anteckningar**

Du kan välja mellan följande `*CropOptions` :

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Du kan välja mellan följande `*PublishJob` :

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

