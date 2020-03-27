---
description: Hämtar resurser som är associerade med en angiven resurs och information om deras relation.
seo-description: Hämtar resurser som är associerade med en angiven resurs och information om deras relation.
seo-title: getAssociatedAssets
solution: Experience Manager
title: getAssociatedAssets
topic: Scene7 Image Production System API
uuid: 70c2f8aa-9104-42b0-b85b-14f90f1ead52
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssociatedAssets{#getassociatedassets}

Hämtar resurser som är associerade med en angiven resurs och information om deras relation.

Syntax

## Auktoriserade användartyper {#section-453cc706400345778713cda249bfac16}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-d11d0dab59e94e89b466123a0ebfa82e}

**Indata (getAssociatedAssetsParam)**

<table id="table_DBB97A6507EB48479FFFD2184FF8F07C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Namn </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatoriskt </p> </th> 
   <th colname="col4" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:sträng</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Hantera till företaget som äger tillgången. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:sträng</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Resurshandtag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:StringArray</span> </p> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Arrayen med önskade svarsfält. Se response- FieldArray/excludeFieldArray i introduktionen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> excludeFieldArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:StringArray</span> </p> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Arrayen med exkluderade svarsfält. Se response- FieldArray/excludeFieldArray i introduktionen. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (getAssociatedAssetsReturn)**

<table id="table_B894B4B6EFA24359A0250A8A4523EA8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Namn </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatoriskt </p> </th> 
   <th colname="col4" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> containerArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AssetArray</span> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Array med set- och mallresurser som innehåller den angivna resursen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AssetArray</span> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Array med resurser som finns i den angivna uppsättningen eller mallresursen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerReferenceArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AssetArray</span> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Array med resurser som refereras i ett lager eller en mall-URL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ownerArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AssetArray</span> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Array med resurser som äger den angivna resursen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> derivedArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AssetArray</span> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Array med resurser som användes för att generera den angivna resursen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatorArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>GeneratorArray <span class="codeph"></span> visar hur den här resursen skapades. Om <span class="codeph"> assetHandler</span> till exempel var en bildsida i en PDF innehåller detta PDF-processorverktyget och refererar till PDF-filresursen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatedArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Den <span class="codeph"> genererade arrayen</span> inverterar det sätt som resursen skapades på. Den <span class="codeph"> genereradeArrayen</span> kan till exempel innehålla en lista med bilder som genererats från den här <span class="codeph"> resurshanteraren</span> om det var en PDF-filresurs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAsset</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:resurs</span> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Information om tumresurs som är associerad med den begärda resursen. Om ingen tumresurs har tilldelats utelämnas fältet i svaret. </p> </td> 
  </tr> 
 </tbody> 
</table>

Du kan använda parametrarna `responseFieldArray` eller `excludeFieldArray` för att begränsa svarsstorleken. I synnerhet är de `GenerationInfo` artiklar som returneras i `generatorArray` eller `generatedArray` som standard inkluderade både upphovspersonen och de genererade tillgångsposterna. För en PDF-resurstyp resulterar det här beteendet i oönskade kopior av PDF-resursposten &quot;original&quot; i svaret. Du kan eliminera problemet genom att lägga `generatedArray/items/originator` till `excludeFieldArray`. Du kan också ange en explicit lista med svarsfält som du vill inkludera i `responseFieldArray`.

## Exempel {#section-8946ea4b9cb94912a8408249c897f192}

Följande grundläggande exempel är en begäran om referensen för generatorn för en bild som extraheras från en PDF-fil. Den innehåller en längd `containerArray` på ett med ett objekt inklusive `assetHandle` PDF-filen.

**Begäran**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|197</beta:assetHandle>
         <beta:responseFieldArray>
            <beta:items>containerArray/items/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**Svar**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <containerArray>
            <items>
               <assetHandle>a|207</assetHandle>
            </items>
         </containerArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

I exemplet ovan finns följande:

**Begäran**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|177</beta:assetHandle>
        <beta:responseFieldArray>
           <beta:items>generatedArray/items/originator/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**Svar**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <generatedArray>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
         </generatedArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

I det här nästa exemplet läggs en grupp till i ett företag med `groupHandleArray`. I det här exemplet används endast en grupp.

**Begäran**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Svar**

Ingen.
