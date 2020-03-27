---
description: Uppdatera fältmetadata.
seo-description: Uppdatera fältmetadata.
seo-title: updateMetadataField
solution: Experience Manager
title: updateMetadataField
topic: Scene7 Image Production System API
uuid: 8712b09b-b02a-4fb3-a0ed-084dc48a717a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateMetadataField{#updatemetadatafield}

Uppdatera fältmetadata.

Syntax

## Auktoriserade användartyper {#section-540e91823fee49a4920ca738f7bfeb99}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-69681ed1ddff437ca1c73f46fe835c96}

**Indata (updateMetadataFieldParam)**

<table id="table_65D6EE6C402E4F01819822A855B6BB7F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameternamn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Obligatoriskt </th> 
   <th colname="col4" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Företagshandtag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Fältreferens för metadata. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> namn</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Namn på metadatafält. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Värde för metadatafält. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Dölj eller visa systemspecifika IPS-metadata. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>En boolesk flagga som anger om metadatafältet används (valideras) när värdet ställs in. </p> <p>Om värdet är true genereras ett fel om ett ogiltigt värde anges i <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Gör att du kan skapa en uppsättning delade uppräknade värden som markerade taggar kan peka på. </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (updateMetadataFieldReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`fieldHandle`*` | `xsd:string` | Ja | Fältreferens för metadata. |

## Exempel {#section-bb7d93ab6d914ddfa294e08983e589ee}

Detta kodexempel uppdaterar tilldelar ett nytt namn och standardvärde till ett metadatafält. Svaret returnerar en referens till det uppdaterade fältet.

**Begäran**

```java
<updateMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
   <name>updateMetadataField</name>
   <defaultValue>Default</defaultValue>
</updateMetadataFieldParam>
```

**Svar**

```java
<updateMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|updateMetadataField</fieldHandle>
</updateMetadataFieldReturn>
```

