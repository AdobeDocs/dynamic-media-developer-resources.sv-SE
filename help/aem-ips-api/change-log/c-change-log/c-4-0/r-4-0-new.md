---
title: Nya tillägg och ändringar
description: Beskriver nya och implementerade ändringar för IPS API v4.0.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 0%

---

# Nya tillägg och ändringar{#new-additions-and-changes}

Beskriver nya och implementerade ändringar för IPS API v4.0.

Implementerade API-versioner sida vid sida med separata WSDL:er och schemanamnutrymmen.

* Tidigare API-versioner: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* SPS 4.0-version: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Tillagd `PostScriptOptions/alpha` fält.

Tillagd `VideoRootUrl` och `SwfRootUrl` egenskaper för `getProperty` operation.

Tillagt som tillval `appName` och `appVersion` parametrar till `authHeader` för att spåra anropande program. Lagt till loggning till `ipsApiService.log`.

Tillagda `serviceUrl` param med WSDL-genereringstjänsten. Den här parametern är användbar för felsökningsutkast. Exempel: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Implementerat `getZipEntries` operation.

Implementerade sökintervall och typbestämda jämförelsevärden för systemfältvillkor.

Tillagd `'Asset'` resurstypssträngskonstant, främst för att tillåta metadatafält mellan resurser.

Implementerat `trashState` param for `searchAssets`.

Implementerat `getAssetPublishHistory` operation.

Tillagt som tillval `faultHttpStatusCode` SOAP-huvud för att aktivera felhantering i Flex. För Flex använder du `<faultHttpStatusCode>200</faultHttpStatusCode>`. Standardstatuskoden för felsvar är `500 (Internal Server Error)`.

Lagt till åtgärder för att återställa resurser från papperskorgen och tomma resurser från papperskorgen.

Implementerade CRUD-åtgärder.

Flagga för aktiverad har lagts till `ImageMap` text och `saveImageMap` operation.

Stöd för Optimera återstående filer.

Tillagd `setAssetsPublishState` för statusuppdateringar för masspublicering.

Tillagd `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Föråldrat `saveMetadataField` till förmån för nya `createMetadataField` och `updateMetadataField` åtgärder.

Implementerat `deleteAssetsParam` gruppborttagningsåtgärd.

Implementerat `moveAssetsParam` gruppflyttningsåtgärd.

Implementerat `deleteMetadataField` operation.

Implementerat `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` åtgärder.

Implementerat `getAssetCounts`.

Utökat stöd för `setImageSetMembers` för `RenderSet` medlemmar i `ImageSet` resurser.

Tillagd `replaceImage` operation.

Tillagd `copyImage` operation.

Tillagd `setUrlModifier` operation och `urlModifier/urlPostApplyModifier` fält för `LayerViewInfo`, `TemplateInfo`och `WatermarkInfo`.

Tillagd `createDerivedAsset` operation. För närvarande `ownerHandle` måste referera till en bildresurs och typen kan `AdjustedView` eller `LayerView`.

Tillagd `createTemplate` operation. Anrop om att skapa mall- eller vattenstämpelresurser.

Inställningar för IPS-företag, `CompanySettings`, som har porterats till API:t för webbtjänster.

Tillagd `excludeByproducts` filterflagga till `searchAssets` operation. Om du anger den här flaggan som true körs den `PSDlayer` bilder och bilder med PDF.

Tillagd `getGenerationInfo` operation.

Tillagd `SystemMessage` egenskapsnamn till `getProperty` operation.

Ändrade vissa strängkonstanter för resurstyp så att de matchade fälten för resursinformation.

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Ändrat resultatformat för gruppåtgärder för att sammanfatta lyckade åtgärder, varningar och fel.

Implementerat `batchSetAssetMetadata` batchmetadataåtgärd.

Implementerat stöd för appspecifika data.

Implementerat stöd för booleska flaggor för `createTemplate`, `extendLayers`och `extractText` för uppladdningsjobb för att styra bearbetningen av Photoshop (på liknande sätt som när du lägger till filöverföringar).

Implementerat `setImageMaps` och `setZoomTargets` åtgärder.

Implementerat `ViewerPreset` åtgärder. De identifierade typerna är:

* `VideoPlayer` (Video publicerar bara dessa visningsprogram.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Skalen i visningsprogrammet har stöd för två parametrar: `skinFg` och `skinBg`. Backend-koden utför all bearbetning som krävs för att bevara bakåtkompatibilitet.

Implementerat `getAssociatedAssets` operation.

Tillagd `ReprocessAssets` jobbtyp för att tillåta ombearbetning av tidigare överförda primära källfiler, inklusive återgivning av PDF och omoptimering av bilder.

Bytt namn `PropertySetType` fälttyp till `propertyType`. Namnändringen påverkar `createPropertySetType` parameter och `getPropertySetType/getPropertySetTypes` svar.

Implementerat `batchSetImageFields` -åtgärd som stöder inställning av bildanvändardata och andra redigerbara bildfält.

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

Implementerat `getActivePublishContexts` operation. Den här åtgärden returnerar en array med publiceringskontextnamn med aktiva publiceringsservrar för det angivna företaget. Aktuella publiceringskontextnamn är:

* `ImageServing`
* `ImageRendering`
* `Video`

Implementerat `getSearchStrings` operation. Den returnerar en array med söksträngar för den angivna resursen.

Lagt till språkparametrar för jobb och en mekanism för att ange språkområde för API-åtgärder. Språkinställningssträngen ska formateras som `<language_code>[-<country_code>]`. Språkkoden är en gemen kod med två bokstäver enligt ISO-639, och den valfria landskoden är en kod med två bokstäver i versaler enligt ISO-3166.

En valfri språkinställningsparameter har lagts till i `authHeader` SOAP-huvud för att ange språkområde för API-åtgärder. Om den här parametern inte finns, kommer HTTP-huvudet `Accept-Language` används. Om den här rubriken inte finns används standardspråket för IPS-servern.

Stöd för get/set har lagts till för metadatafält med starkt typsnitt.

Implementerat stöd för SOAP och HTTP-huvud för GZIP-svarskontroll.

Tillagd `gzipResponse` flagga till `authHeader`. Om det inte finns kontrollerar API:t HTTP `Accept-Encoding` header.

Stöd har lagts till i searchAssets för väldigt typbestämda villkor för metadatafält.

* För alla fälttyper kan värdet skickas med en strängjämförelseoperator ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* För booleska fält `boolVal` kan passera med `Equals` Uppe.
* Int-fält `longVal` kan skickas med en numerisk jämförelseoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) eller `minLong/maxLong` kan skickas med numeriska operationer ( `Between, NotBetween`).
* För flyttbara fält, `doubleVal` kan skickas med en numerisk jämförelseoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) eller `minDouble/maxDouble` kan skickas med numeriska operationer ( `Between, NotBetween`).
* För datumfält kan du skicka `dateVal` med en numerisk jämförelseoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) eller du kan skicka minDate/maxDate med numeriska intervallåtgärder ( `Between, NotBetween`).

Tillagd beskrivning, `jobSubType`och `originalJobName` fält till `JobLog` typ.

* `originalJobName` är jobbnamnet som skickas till `submitJob` (utan unika suffix eller efternamn).
* `jobSubType` används endast av `ImageServingPublishJob` jobb (där det är ett av `full`, `increment, fullwithsearch,` eller `fulloverride`).
* `description` är en tom sträng för alla jobbtyper, men innehåller så småningom information om sammanfattningsjobb, som överföringssökvägen.

Dessutom ingår inte följande fält i båda `getJobLogs` och `getJobLogDetails`. I tidigare versioner var de bara tillgängliga med `getJobLogDetails`.

* `endDate` (om jobbet har slutförts).
* `fileDuplicateCount` (tidigare var det alltid `0` med `getJobLogs`)
* `fileUpdateCount` (tidigare alltid `0` med `getJobLogs` och ingår i `fileSuccessCount`; delas nu upp i separata fält).

Tillagt AssetHandle-fält i `JobLogDetail` typ.

En valfri beskrivningsparameter har lagts till i `submitJob`. Den här parametern skickas för hämtning i `getScheduledJobs`, `getActiveJobs`och `getJobLogs`.

SKU-systemfältet är inaktuellt. Fältet ignoreras om det skickas som en `SystemFieldCondition` till `searchAssets`.

Tillagd `excludeAssetTypeArray` filtrera till `searchAssets`.

Tillagd `MaskInfo` skriv till `Asset`.

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
   <td colname="col2"> <p>Adobe Illustrator-fil. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>EPS- och PostScript-filer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® Word-dokument för filer som slutar med .doc. </p> </td> 
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

Ytterligare alternativ har lagts till i `UploadDirectoryJob` och `UploadUrlsJob` för att styra bearbetningen av PostScript-, Illustrator- och PDF-filer oberoende av varandra. Alla befintliga jobb ger de nödvändiga parametrarna till var och en av de tre bearbetningsledningarna så att de fungerar exakt som i dag. Originalet `PostScriptOptions` -blocket används för att ange bearbetningen för Illustrator- och EPS/PS-filer. Alternativt kan du ange speciella filalternativblock för bearbetning. Listan över ändringar innehåller:

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> process </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Ingen </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rastrera </span>(standard) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Hantera bara tillgången och skapa inga derivat vid överföring. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Rendera EPS- och PostScript-filen till en bild med den angivna upplösningen och färgrymden. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Valfritt. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Börjar gälla när filen rastreras till en bild. En genomskinlig bakgrund skapas om originalfilen definieras på det här sättet för att täcka över logotyper. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions </span> </p> </td> 
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
   <td colname="col2"> <p> <span class="codeph"> upplösning </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rastrerar upplösningen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> färgrymd </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Målfärgrymd för återgivning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Valfritt. </p> </td> 
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
   <td colname="col2"> <p> <span class="codeph"> upplösning </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rastrerar upplösningen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> färgrymd </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Målfärgrymd för återgivning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definierar om en flersidig PDF ska kombineras i en e-katalog efter återgivningen (standardvärdet är true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definierar om ord från PDF ska extraheras till databasen för att senare skickas till en sökserver (standardvärdet är false). </p> </td> 
  </tr> 
 </tbody> 
</table>

Du kan även hämta frågor från `getScheduledJobs`.

Ändrad `webservice.gzip.response` konfigurationsegenskap så att något av följande värden används:

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Värde </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> aldrig </span> </p> </td> 
   <td colname="col2"> <p>Gzip-svar får inte ges. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> soppa </span> </p> </td> 
   <td colname="col2"> <p>Gzip-svar endast om authHeader/gzipResponse är true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> acceptera </span> </p> </td> 
   <td colname="col2"> <p>Gzip om authHeader/gzipResponse är true, eller ingen gzipResponse-rubrik finns och HTTP Accept-Encoding-huvudet innehåller gzip. (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alltid </span> </p> </td> 
   <td colname="col2"> <p>Gzip-svar alltid, oavsett rubrikvärden. Använd det här värdet endast i felsökningssyfte. </p> </td> 
  </tr> 
 </tbody> 
</table>
