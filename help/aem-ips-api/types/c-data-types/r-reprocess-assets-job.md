---
description: Jobbtyp som tillåter ombearbetning av tidigare överförda primära filer, inklusive återgivning av PDF och återoptimering av bilder.
solution: Experience Manager
title: ÅterbearbetaResurserJobb
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6078246-54e1-4119-b4f8-ba6a28577cff
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# [!DNL ReprocessAssetsJob]{#reprocessassetsjob}

Jobbtyp som tillåter ombearbetning av tidigare överförda primära filer, inklusive återgivning av PDF och återoptimering av bilder.

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Resurshandtag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolesk</span> </p> </td> 
   <td colname="col3"> <p>Anger om filerna är markerade som klara för publicering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolesk</span> </p> </td> 
   <td colname="col3"> <p>Styr om publiceringstillståndet för en befintlig resurs bevaras när den skrivs över. Om den inte anges används företagets standardinställning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolesk</span> </p> </td> 
   <td colname="col3"> <p>Om en mask ska skapas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolesk</span> </p> </td> 
   <td colname="col3"> <p>Kontrollerar bevarande av befintliga beskärningsdefinitioner. Standardvärdet är true.</p> <p>Om du anger parametern manualCropOptions och motsvarande värden används de nya värdena (exklusive 0,0,0,0) för resursen oavsett preserveCrop-värdet.</p><p>Om du <i>inte</i> anger parametern manualCropOptions behålls värdet för preserveCrop. Om värdet är true behålls de befintliga preserveCrop-värdena. Om värdet är false tas preserveCrop-värdena bort.</p><p>Exempel:</p><p><p>&lt;preserveCrop&gt;false&lt;/preserveCrop&gt;<br />&lt;manualCropOptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualCropOptions&gt;</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Manuella beskärningsalternativ. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ för automatisk beskärning av bilder baserat på färg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Tar bort tomt utrymme från bildkanterna baserat på genomskinlighet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ för överföring av Photoshop-filer till Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ för överföring av PostScript-filer till Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ för överföring av PDF-filer till Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ för A/V-mediefiler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ för överföring av Illustrator-filer till Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ som du kan ange under en överföring. Uppsättningen påverkar hur färgen hanteras för överföringen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>En matris med skript för automatisk set-generering som ska användas för överförda filer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>En array med projektreferenser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Alternativ för e-postinställningar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolesk</span> </p> </td> 
   <td colname="col3"> <p>Om bara filer ska överföras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>URL till filöverföringsplats. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Jobbinformation för en bild som visar ett publiceringsjobb som ska köras när överföringen är slutförd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Jobbinformation för ett publiceringsjobb för bildåtergivning som ska köras när överföringen är slutförd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Jobbinformation för ett videopubliceringsjobb som ska köras när överföringen är slutförd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ för överföring av InDesign till bildservern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knockoutBackground </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Maskera bakgrunden för markerade bilder. På så sätt kan du täcka över dem i andra lager med en genomskinlighet utanför objektbilden. </p> <p>Valfritt. </p> <p>Se <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unsharpMaskOptions </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:UnsharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>Alternativ som gör att du kan styra inställningarna för oskarp mask när du skapar en optimerad TIF-pyramidfil. Använd de här inställningarna för att förbättra bildens skärpa. </p> <p>Se <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html?lang=sv-SE"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Anteckningar**

Alternativ för `*CropOptions` inkluderar:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Alternativ för `*PublishJob` inkluderar:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`
