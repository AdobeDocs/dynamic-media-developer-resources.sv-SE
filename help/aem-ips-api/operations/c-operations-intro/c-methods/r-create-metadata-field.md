---
description: Gör att administratörer kan skapa nya metadatafält som kan koordineras med content management-system eller för mallåtgärder. Exempel på skapade metadatafält är nyckelord, information om författaren till bilden eller information om upphovsrättsinnehavare.
seo-description: Gör att administratörer kan skapa nya metadatafält som kan koordineras med content management-system eller för mallåtgärder. Exempel på skapade metadatafält är nyckelord, information om författaren till bilden eller information om upphovsrättsinnehavare.
seo-title: createMetadataField
solution: Experience Manager
title: createMetadataField
topic: Scene7 Image Production System API
uuid: 50ab61fa-df44-4305-ad9f-693c4aea1e69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createMetadataField{#createmetadatafield}

Gör att administratörer kan skapa nya metadatafält som kan koordineras med content management-system eller för mallåtgärder. Exempel på skapade metadatafält är nyckelord, information om författaren till bilden eller information om upphovsrättsinnehavare.

Syntax

## Auktoriserade användartyper {#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## Parametrar {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**Indata (createMetadataFieldParam)**

<table id="table_E5B249BBED3B4D2F9CEE2CCF27472D1B"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Namnet på det företag som metadatafältet tillhör. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Resurstyp. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> namn</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Namnet på metadatafältet som du skapar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4">Typ av metadatafält. <p>Metadatafältstyperna definierar de tillgängliga typerna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Standardvärdet för metadatafältet som ska skapas (till exempel <span class="codeph"> Scen 7</span>). </p> <p>Standardvärden stöds inte för taggfältstyper och måste utelämnas. Om ett icke-tomt standardvärde anges för en taggfältstyp returneras ett fel. </p> </td> 
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

**Utdata (createMetadataFieldReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`fieldHandle`*` | `xsd:string` | Ja | Referensen till det nya metadatafältet. |

## Exempel {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

Detta kodexempel skapar ett metadatafält för strängtyp med namnet `createMetadataField`. Svaret returnerar referensen till det nya metadatafältet.

**Begäran**

```java
<createMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetType>Image</assetType>
   <name>createMetadataField</name>
   <fieldType>String</fieldType>
   <initialTagValue>Fall</initialTagValue>
   <defaultValue>Default</defaultValue>
</createMetadataFieldParam>
```

**Svar**

```java
<createMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
</createMetadataFieldReturn>
```

