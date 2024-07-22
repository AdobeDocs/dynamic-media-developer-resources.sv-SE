---
title: Nya tillägg och ändringar
description: Beskriver nya och implementerade ändringar för IPS API v4.0.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '1199'
ht-degree: 0%

---

# Nya tillägg och ändringar{#new-additions-and-changes}

Beskriver nya och implementerade ändringar för IPS API v4.0.

Implementerade API-versioner sida vid sida med separata WSDL:er och schemanamnutrymmen.

* Tidigare API-versioner: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* SPS 4.0-version: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

`PostScriptOptions/alpha` fält har lagts till.

`VideoRootUrl`- och `SwfRootUrl`-egenskaper för åtgärden `getProperty` har lagts till.

Valfria `appName`- och `appVersion`-parametrar har lagts till i `authHeader` för att spåra anropande program. Loggning har lagts till i `ipsApiService.log`.

En valfri `serviceUrl`-parameter har lagts till i WSDL-genereringstjänsten. Den här parametern är användbar för felsökningsutkast. Till exempel: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Åtgärden `getZipEntries` har implementerats.

Implementerade sökintervall och typbestämda jämförelsevärden för systemfältvillkor.

`'Asset'`-resurstypsträngskonstant har lagts till, främst för att tillåta metadatafält för korsresurser.

Implementerade `trashState`-param för `searchAssets`.

Åtgärden `getAssetPublishHistory` har implementerats.

Det valfria huvudet `faultHttpStatusCode` SOAP har lagts till för att aktivera felhantering i Flex. Använd `<faultHttpStatusCode>200</faultHttpStatusCode>` för Flex. Standardstatuskoden för felsvar är `500 (Internal Server Error)`.

Lagt till åtgärder för att återställa resurser från papperskorgen och tomma resurser från papperskorgen.

Implementerade CRUD-åtgärder.

Flagga som är aktiverad har lagts till i åtgärden `ImageMap` och `saveImageMap`.

Stöd för Optimera återstående filer.

`setAssetsPublishState` har lagts till för statusuppdateringar för masspublicering.

`ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings` har lagts till.

`saveMetadataField`-åtgärden har tagits bort till förmån för nya `createMetadataField`- och `updateMetadataField`-åtgärder.

`deleteAssetsParam` batchborttagningsåtgärd har implementerats.

`moveAssetsParam` gruppflyttningsåtgärd har implementerats.

Åtgärden `deleteMetadataField` har implementerats.

`get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` åtgärder har implementerats.

Implementerad `getAssetCounts`.

Stöd har lagts till för `setImageSetMembers` för att inkludera `RenderSet` medlemmar i `ImageSet`-resurser.

`replaceImage`-åtgärden har lagts till.

`copyImage`-åtgärden har lagts till.

`setUrlModifier`-åtgärd och `urlModifier/urlPostApplyModifier` fält för `LayerViewInfo`, `TemplateInfo` och `WatermarkInfo` har lagts till.

`createDerivedAsset`-åtgärden har lagts till. För närvarande måste `ownerHandle` referera till en bildresurs och typen kan vara `AdjustedView` eller `LayerView`.

`createTemplate`-åtgärden har lagts till. Anrop om att skapa mall- eller vattenstämpelresurser.

Företagsinställningar för IPS, `CompanySettings`, som har porterats till API:t för webbtjänster.

`excludeByproducts` filterflagga har lagts till i åtgärden `searchAssets`. Om du anger den här flaggan som true körs `PSDlayer` bilder och bilder som har rippats i PDF.

`getGenerationInfo`-åtgärden har lagts till.

Egenskapsnamnet `SystemMessage` har lagts till i åtgärden `getProperty`.

Ändrade vissa strängkonstanter för resurstyp så att de matchade fälten för resursinformation.

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Ändrat resultatformat för gruppåtgärder för att sammanfatta lyckade åtgärder, varningar och fel.

`batchSetAssetMetadata` batchmetadataåtgärd har implementerats.

Implementerat stöd för appspecifika data.

Implementerat stöd för booleska flaggor för `createTemplate`, `extendLayers` och `extractText` för överföringsjobb för att styra bearbetningen av Photoshop (på liknande sätt som ändringar för filöverföringar).

Implementerade `setImageMaps`- och `setZoomTargets`-åtgärder.

`ViewerPreset` åtgärder har implementerats. De identifierade typerna är:

* `VideoPlayer` (Video publicerar bara dessa visningsprogram.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Visningsprogrammets skal har stöd för två parametrar: `skinFg` och `skinBg`. Backend-koden utför all bearbetning som krävs för att bevara bakåtkompatibilitet.

Åtgärden `getAssociatedAssets` har implementerats.

`ReprocessAssets`-jobbtypen har lagts till för att tillåta ombearbetning av tidigare överförda primära källfiler, inklusive återställande av PDF och omoptimering av bilder.

Fälttypen `PropertySetType` har bytt namn till `propertyType`. Namnändringen påverkar parametern `createPropertySetType` och svaret på `getPropertySetType/getPropertySetTypes`.

Åtgärden `batchSetImageFields` har implementerats för att ge stöd för inställning av bildanvändardata och andra redigerbara bildfält.

47 Lagt till filstorleksfält till olika typer av tillgångsinformation:

* `VignetteInfo`
* `CabinetInfo`
* `WindowCoveringInfo`
* `IccProfileInfo`
* `FontInfo`
* `XslInfo`
* `ViewerSwfInfo`
* `XmlInfo`
* `SvgInfo`
* `ZipInfo`
* `VideoInfo`
* `AcoInfo`
* `PdfInfo`
* `PsdInfo`
* `FlashInfo`
* `InDesignInfo`
* `PostScriptInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `RTFInfo`

Åtgärden `getActivePublishContexts` har implementerats. Den här åtgärden returnerar en array med publiceringskontextnamn med aktiva publiceringsservrar för det angivna företaget. Aktuella publiceringskontextnamn är:

* `ImageServing`
* `ImageRendering`
* `Video`

Åtgärden `getSearchStrings` har implementerats. Den returnerar en array med söksträngar för den angivna resursen.

Lagt till språkparametrar för jobb och en mekanism för att ange språkområde för API-åtgärder. Språksträngen ska formateras som `<language_code>[-<country_code>]`. Språkkoden är en gemen kod med två bokstäver enligt ISO-639, och den valfria landskoden är en kod med två bokstäver i versaler enligt ISO-3166.

En valfri språkinställningsparameter har lagts till i SOAP `authHeader` för att ange språkinställningen för API-åtgärder. Om den här parametern inte finns används HTTP-huvudet `Accept-Language`. Om den här rubriken inte finns används standardspråket för IPS-servern.

Stöd för get/set har lagts till för metadatafält med starkt typsnitt.

Implementerat stöd för SOAP och HTTP-huvud för GZIP-svarskontroll.

`gzipResponse`-flaggan har lagts till i `authHeader`. Om den inte finns kontrollerar API:t HTTP `Accept-Encoding`-huvudet.

Stöd har lagts till i searchAssets för väldigt typbestämda villkor för metadatafält.

* För alla fälttyper kan värdet skickas med en strängjämförelseoperator ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* För booleska fält kan `boolVal` skickas med `Equals`-operatorn.
* För Int-fält kan `longVal` skickas med en numerisk jämförelseoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) eller så kan `minLong/maxLong` skickas med en numerisk intervallåtgärd ( `Between, NotBetween`).
* För flyttalsfält kan `doubleVal` skickas med en numerisk jämförelseoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) eller så kan `minDouble/maxDouble` skickas med en numerisk intervallåtgärd ( `Between, NotBetween`).
* För datumfält kan du skicka `dateVal` med en numerisk jämförelseoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) eller skicka minDate/maxDate med numeriska intervallåtgärder ( `Between, NotBetween`).

Beskrivnings-, `jobSubType`- och `originalJobName`-fält har lagts till i typen `JobLog`.

* `originalJobName` är jobbnamnet som skickas till `submitJob` (utan unika suffix eller efterföljande jobbnamn).
* `jobSubType` används bara av `ImageServingPublishJob` jobb (där det är något av `full`, `increment, fullwithsearch,` eller `fulloverride`).
* `description` är en tom sträng för alla jobbtyper, men innehåller så småningom information om sammanfattningsjobb, som överföringssökvägen.

Dessutom ingår inte följande fält i både `getJobLogs` och `getJobLogDetails`. I tidigare versioner var de bara tillgängliga med `getJobLogDetails`.

* `endDate` (om jobbet har slutförts).
* `fileDuplicateCount` (tidigare var det alltid `0` med `getJobLogs`)
* `fileUpdateCount` (tidigare var alltid `0` med `getJobLogs` och inkluderad i `fileSuccessCount`; den delas nu upp i separata fält).

Tillagt AssetHandle-fält till typen `JobLogDetail`.

En valfri beskrivningsparameter har lagts till i `submitJob`. Den här parametern skickas för hämtning i `getScheduledJobs`, `getActiveJobs` och `getJobLogs`.

SKU-systemfältet är inaktuellt. Fältet ignoreras om det skickas som en `SystemFieldCondition` till `searchAssets`.

`excludeAssetTypeArray` har lagts till i `searchAssets`.

`MaskInfo`-typen har lagts till i `Asset`.

Nya tillgångstyper har lagts till för hantering av IPS:

<table id="table_DCCE936B797A448598C30E3B344525A5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Tillgångstyp </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Illustrator </span> </p> </td> 
   <td colname="col2"> <p>Adobe Illustrator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>EPS och PostScript. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® Word för filer som slutar med .doc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® Excel-dokument för filer som slutar med .xls. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® PowerPoint-dokument för filer som slutar med .ppt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>RTF-fil för filer som överförts och som slutar med .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ytterligare alternativ har lagts till i `UploadDirectoryJob` och `UploadUrlsJob` för att styra bearbetningen av PostScript-, Illustrator- och PDF-filer oberoende av varandra. Alla befintliga jobb ger de nödvändiga parametrarna till var och en av de tre bearbetningsledningarna så att de fungerar exakt som i dag. Det ursprungliga `PostScriptOptions`-blocket används för att ställa in bearbetningen för Illustrator- och EPS/PS-filer. Alternativt kan du ange speciella filalternativblock för bearbetning. Listan över ändringar innehåller:

<table id="table_D4E5ACCB2D144D05A5FA0129AA5F9344"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Fält </p> </th> 
   <th colname="col2" class="entry"> <p>Parameter </p> </th> 
   <th colname="col3" class="entry"> <p>Värde </p> </th> 
   <th colname="col4" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> <p> <span class="codeph"> [!DNL PostScriptOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL process] </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Ingen </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rastrera </span> (standard) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Hantera bara tillgången och skapa inga derivat vid överföring. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Rendera EPS- och PostScript-filen till en bild med den angivna upplösningen och färgrymden. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa </span> </p> <p>Valfritt. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolesk&gt; </span> </p> </td> 
   <td colname="col4"> <p>Börjar gälla när filen rastreras till en bild. En genomskinlig bakgrund skapas om originalfilen definieras på det här sättet för att täcka över logotyper. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> [!DNL IllustratorOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> process </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Ingen </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rastrera </span> (standard) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Hantera bara tillgången och skapa inga derivat vid överföring. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Rendera filen i en bild med den angivna upplösningen och färgrymden. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;heltal&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rastrerar upplösningen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Målfärgrymd för återgivning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alfa </span> </p> <p>Valfritt. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Börjar gälla när filen rastreras till en bild. Skapar en genomskinlig bakgrund om originalfilen definieras på det här sättet för att skapa överliggande logotyper. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> process </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Ingen </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rastrera </span> (standard) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Hantera bara tillgången och skapa inga derivat vid överföring. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Rendera filen i en bild med den angivna upplösningen och färgrymden. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;heltal&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rastrerar upplösningen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Målfärgrymd för återgivning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolesk&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definierar om en flersidig PDF ska kombineras i en e-katalog efter återgivningen (standardvärdet är true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolesk&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definierar om ord från PDF ska extraheras till databasen för att senare skickas till en sökserver (standardvärdet är false). </p> </td> 
  </tr> 
 </tbody> 
</table>

Du kan även fråga från `getScheduledJobs`.

Konfigurationsegenskapen `webservice.gzip.response` har ändrats så att något av följande värden används:

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Värde </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL never] </span> </p> </td> 
   <td colname="col2"> <p>Gzip-svar får inte ges. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL soap] </span> </p> </td> 
   <td colname="col2"> <p>Gzip-svar endast om authHeader/gzipResponse är true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL accept] </span> </p> </td> 
   <td colname="col2"> <p>Gzip om authHeader/gzipResponse är true, eller ingen gzipResponse-rubrik finns och HTTP Accept-Encoding-huvudet innehåller gzip. (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL always] </span> </p> </td> 
   <td colname="col2"> <p>Gzip-svar alltid, oavsett rubrikvärden. Använd det här värdet endast i felsökningssyfte. </p> </td> 
  </tr> 
 </tbody> 
</table>
