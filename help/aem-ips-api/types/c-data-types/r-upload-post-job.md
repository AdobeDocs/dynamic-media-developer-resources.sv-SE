---
description: Använder getActiveJobs för att spåra skrivbordsöverföringar.
seo-description: Använder getActiveJobs för att spåra skrivbordsöverföringar.
seo-title: UploadPostJob
solution: Experience Manager
title: UploadPostJob
topic: Scene7 Image Production System API
uuid: 172f47c7-685a-4014-9c30-dacd78733655
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UploadPostJob{#uploadpostjob}

Använder getActiveJobs för att spåra skrivbordsöverföringar.

Se även [Överföra resurser via HTTP POST till överföring...](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>Alla POST-begäranden för ett överföringsjobb måste komma från samma IP-adress.

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Namn </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col03" class="entry"> <p>Obligatoriskt? </p> </th> 
   <th colname="col3" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AutoColorCropOptions</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Alternativ för automatisk beskärning av bilder baserat på färg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AutoSetCreateOptions</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>En matris med skript för automatisk set-generering som ska användas för överförda filer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AutoTransparentCropOptions</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Tar bort tomt utrymme från bildkanterna baserat på genomskinlighet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ColorManagementOptions</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Alternativ som du kan ange under en överföring. Uppsättningen påverkar hur färgen hanteras för överföringen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col03"> <p><b>Ja</b> </p> </td> 
   <td colname="col3"> <p>Om en mask ska skapas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col03"> <p><b>Ja</b> </p> </td> 
   <td colname="col3"> <p>Val av e-postinställningar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:InDesignOptions</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Alternativ för överföring av InDesign-filer till Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:IllustratorOptions</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Alternativ för överföring av Illustrator-filer till Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:KnockoutBackgroundOptions</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Maskera bakgrunden för markerade bilder. På så sätt kan du täcka över dem i andra lager med en genomskinlighet utanför objektbilden. Valfritt. </p> <p>Se<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ManualCropOptions</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Alternativ för manuell beskärning av bilder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:MediaOptions</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Alternativ som gör att du kan ange en miniatyrbild från videon. </p> <p>Se <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> Mediealternativ</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> skriv över</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col03"> <p><b>Ja</b> </p> </td> 
   <td colname="col3"> <p>Om filer ska skrivas över vid överföring. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:PDFOptions</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Alternativ för överföring av PDF-filer till bildservern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:PhotoshopOptions</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Alternativ för att överföra Photoshop-filer till bildservern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Den URL som filerna överförs till. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:PostScriptOptions</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Alternativ för överföring av PostScript-filer till Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Kontrollerar bevarande av befintliga beskärningsdefinitioner. Standardvärdena är true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col03"> <p><b>Ja</b> </p> </td> 
   <td colname="col3"> <p>Styr om publiceringstillståndet för en befintlig resurs bevaras när den skrivs över. Om den inte anges används företagets standardinställning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:HandleArray</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Array med projektreferenser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col03"> <p><b>Ja</b> </p> </td> 
   <td colname="col3"> <p>Anger om filerna är markerade som klara för publicering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:UnCompressOptions</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Extrahera och bearbeta innehållet i överförda TAR/ZIP-filer med dessa valfria inställningar. </p> <p>Se <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> AvkomprimeraAlternativ</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:UnsharpMaskOptions</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Alternativ som gör att du kan styra inställningarna för oskarp mask när du skapar en optimerad TIF-pyramidfil. Använd de här inställningarna för att förbättra bildens skärpa. </p> <p>Se <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col03"> <p>Nej </p> </td> 
   <td colname="col3"> <p>Ytterligare ett metadataalternativ för allt i överföringsjobbet. </p> </td> 
  </tr> 
 </tbody> 
</table>

